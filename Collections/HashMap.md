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

```

## Question 47: Create a HashMap of city names to populations

```java

```

## Question 48: Create a HashMap of product names to prices

```java

```

## Question 49: Create a HashMap of employee IDs to departments

```java

```
