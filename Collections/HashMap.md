# Java Collections: HashMap

## Question 45: Create a HashMap of country names to capitals

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

## Question 46: Create a HashMap of employee IDs to names

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        Map<Integer, String> map = new HashMap<>();
        map.put(101, "Aman");
        map.put(102, "Riya");
        map.put(103, "Kabir");

        System.out.println(map.get(102));
        for (Map.Entry<Integer, String> e : map.entrySet()) {
            System.out.println(e.getKey() + " -> " + e.getValue());
        }
    }
}
```

## Question 47: Create a HashMap of city names to populations

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        Map<String, Integer> map = new HashMap<>();
        map.put("Delhi", 32000000);
        map.put("Mumbai", 21000000);
        map.put("Pune", 7000000);

        System.out.println(map.get("Mumbai"));
        System.out.println(map.getOrDefault("Goa", 0));
        for (String city : map.keySet()) {
            System.out.println(city + " -> " + map.get(city));
        }
    }
}
```

## Question 48: Create a HashMap of product names to prices

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        Map<String, Double> map = new HashMap<>();
        map.put("pen", 10.5);
        map.put("book", 120.0);
        map.put("bag", 899.99);

        System.out.println(map.get("book"));
        for (Map.Entry<String, Double> e : map.entrySet()) {
            System.out.println(e.getKey() + " -> " + e.getValue());
        }
    }
}
```

## Question 49: Create a HashMap of employee IDs to departments

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        Map<Integer, String> map = new HashMap<>();
        map.put(101, "Sales");
        map.put(102, "HR");
        map.put(103, "Engineering");

        System.out.println(map.get(103));
        System.out.println(map.containsKey(104));
        for (int id : map.keySet()) {
            System.out.println(id + " -> " + map.get(id));
        }
    }
}
```
