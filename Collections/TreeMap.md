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

```

## Question 33: Create a TreeMap of student IDs to their details

```java

```
