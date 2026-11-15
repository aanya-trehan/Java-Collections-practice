# Java Collections: TreeMap

## Question 30: Create a TreeMap, add elements, print in sorted order of keys

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        TreeMap<Integer, String> map = new TreeMap<>();
        map.put(3, "c");
        map.put(1, "a");
        map.put(2, "b");

        System.out.println(map);
    }
}
```

## Question 31: Create a TreeMap of book titles to their authors

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        TreeMap<String, String> map = new TreeMap<>();

        map.put("abc", "reg5hg5h");
        map.put("bcd", "rfrf");
        map.put("aweefc", "rfgreg");

        for (String key : map.keySet()) {
            System.out.println("key " + key + " value " + map.get(key));
        }
    }
}
```

## Question 32: Create a TreeMap of words to their frequencies in a given text

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        String text = "the cat and the dog and the bird";

        Map<String, Integer> freq = new TreeMap<>();
        for (String word : text.split(" ")) {
            freq.put(word, freq.getOrDefault(word, 0) + 1);
        }

        System.out.println(freq);
    }
}
```

## Question 33: Create a TreeMap of student IDs to their details

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        Map<Integer, String> students = new TreeMap<>();
        students.put(103, "Riya");
        students.put(101, "Aman");
        students.put(102, "Kabir");

        System.out.println(students.get(102));
        for (Map.Entry<Integer, String> e : students.entrySet()) {
            System.out.println(e.getKey() + " -> " + e.getValue());
        }
    }
}
```
