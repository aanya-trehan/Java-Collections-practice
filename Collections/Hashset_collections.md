# Java Collections: HashSet

## Question 14: Create a HashSet, add elements, and print them

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        Set<String> fruits = new HashSet<>();
        fruits.add("apple");
        fruits.add("banana");
        fruits.add("mango");
        fruits.add("apple");

        System.out.println(fruits);
        for (String f : fruits) {
            System.out.println(f);
        }
    }
}
```

## Question 15: Check if a particular element exists in a HashSet

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        Set<Integer> set = new HashSet<>(Arrays.asList(10, 20, 30));

        System.out.println(set.contains(20));
        System.out.println(set.contains(99));

        if (set.contains(30)) {
            System.out.println("30 is present");
        }
    }
}
```

## Question 16: Create a HashMap of country names to capitals

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        Map<String, String> capitals = new HashMap<>();
        capitals.put("India", "New Delhi");
        capitals.put("France", "Paris");
        capitals.put("Japan", "Tokyo");

        System.out.println(capitals.get("France"));
        System.out.println(capitals.containsKey("Japan"));
        System.out.println(capitals.getOrDefault("Peru", "unknown"));

        for (Map.Entry<String, String> e : capitals.entrySet()) {
            System.out.println(e.getKey() + " -> " + e.getValue());
        }
    }
}
```

## Question 17: Find the common elements between two ArrayLists

Solution 1: keeps repeats from the first list

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        List<Integer> a = new ArrayList<>(Arrays.asList(1, 2, 2, 3, 4));
        List<Integer> b = new ArrayList<>(Arrays.asList(2, 4, 6));

        List<Integer> common = new ArrayList<>(a);
        common.retainAll(b);

        System.out.println(common);
    }
}
```

Solution 2: each common value once

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        List<Integer> a = new ArrayList<>(Arrays.asList(1, 2, 2, 3, 4));
        List<Integer> b = new ArrayList<>(Arrays.asList(2, 4, 6));

        Set<Integer> lookup = new HashSet<>(b);
        Set<Integer> common = new HashSet<>();
        for (int x : a) {
            if (lookup.contains(x)) {
                common.add(x);
            }
        }

        System.out.println(common);
    }
}
```

## Question 18: Create a TreeMap of words to their frequencies in a text

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

## Question 19: Check if a HashSet is a subset of another HashSet

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        Set<Integer> big = new HashSet<>(Arrays.asList(1, 2, 3, 4, 5));
        Set<Integer> small = new HashSet<>(Arrays.asList(2, 4));
        Set<Integer> other = new HashSet<>(Arrays.asList(2, 9));

        System.out.println(big.containsAll(small));
        System.out.println(big.containsAll(other));
    }
}
```
