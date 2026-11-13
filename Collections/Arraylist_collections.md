# Java Collections: ArrayList

## Question 1: Sort an ArrayList of Strings alphabetically

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        ArrayList<String> arr = new ArrayList<>();
        arr.add("apple");
        arr.add("orange");
        arr.add("cucumber");

        Collections.sort(arr);

        System.out.println(arr);
    }
}
```

## Question 2: Find the maximum element from an ArrayList of Integers

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        List<Integer> arr = Arrays.asList(1, 2, 3, 4, 5, 6, 1, 2, 2, 8);

        int max = Collections.max(arr);

        System.out.println("Maximum element: " + max);
    }
}
```

## Question 3: Remove all duplicate elements from an ArrayList

Solution 1: build a new list

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        List<Integer> arr = new ArrayList<>(Arrays.asList(1, 2, 3, 1, 2, 2, 8));

        LinkedHashSet<Integer> set = new LinkedHashSet<>(arr);

        ArrayList<Integer> unique = new ArrayList<>(set);

        System.out.println(unique);
    }
}
```

Solution 2: change the same list

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        List<Integer> list = new ArrayList<>(Arrays.asList(1, 2, 3, 1, 2, 2, 8));

        Set<Integer> set = new HashSet<>(list);
        list.clear();
        list.addAll(set);

        System.out.println(list);
    }
}
```

## Question 4: Create a LinkedList and perform add, remove and iterate

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        LinkedList<String> list = new LinkedList<>();

        list.add("a");
        list.add("b");
        list.add("c");
        list.addFirst("start");

        list.remove("b");
        list.removeFirst();

        for (String s : list) {
            System.out.println(s);
        }

        Iterator<String> it = list.iterator();
        while (it.hasNext()) {
            System.out.println(it.next());
        }
    }
}
```

## Question 5: Find the intersection of two ArrayLists

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        List<Integer> a = new ArrayList<>(Arrays.asList(1, 2, 3, 4, 5));
        List<Integer> b = new ArrayList<>(Arrays.asList(3, 4, 5, 6, 7));

        List<Integer> common = new ArrayList<>(a);
        common.retainAll(b);

        System.out.println(common);
    }
}
```

## Question 6: Shuffle the elements of an ArrayList

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        List<Integer> list = new ArrayList<>(Arrays.asList(1, 2, 3, 4, 5));

        Collections.shuffle(list);
        System.out.println(list);

        Collections.shuffle(list, new Random(42));
    }
}
```

## Question 7: Find the second-largest element in an ArrayList of Integers

Solution 1: Collections.sort

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        List<Integer> list = new ArrayList<>(Arrays.asList(1, 2, 3, 4, 5, 6, 1, 2, 2, 8));

        Collections.sort(list);

        int largest = list.get(list.size() - 1);
        int i = list.size() - 2;

        while (i >= 0 && list.get(i) == largest) {
            i--;
        }

        System.out.println("Second largest: " + list.get(i));
    }
}
```

Solution 2: TreeSet

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        List<Integer> list = Arrays.asList(1, 2, 3, 4, 5, 6, 1, 2, 2, 8);

        TreeSet<Integer> set = new TreeSet<>(list);

        set.pollLast();

        System.out.println("Second largest: " + set.last());
    }
}
```

## Question 8: Find the frequency of each element in an ArrayList

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        List<Integer> list = Arrays.asList(1, 2, 3, 4, 5, 6, 1, 2, 2, 8);

        Map<Integer, Integer> freq = new HashMap<>();

        for (int n : list) {
            freq.put(n, freq.getOrDefault(n, 0) + 1);
        }

        System.out.println(freq);
    }
}
```

## Question 9: Find the kth smallest element in an ArrayList

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        List<Integer> list = new ArrayList<>(Arrays.asList(7, 10, 4, 3, 20, 15));
        int k = 3;

        List<Integer> sorted = new ArrayList<>(list);
        Collections.sort(sorted);

        System.out.println(sorted.get(k - 1));
    }
}
```

## Question 10: Merge two ArrayLists into a single ArrayList

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        List<Integer> a = Arrays.asList(1, 2, 3);
        List<Integer> b = Arrays.asList(4, 5, 6);

        List<Integer> merged = new ArrayList<>(a);
        merged.addAll(b);

        System.out.println(merged);
    }
}
```

## Question 11: Find the intersection of multiple Sets

Solution 1: a few sets

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        Set<Integer> s1 = new HashSet<>(Arrays.asList(1, 2, 3, 4));
        Set<Integer> s2 = new HashSet<>(Arrays.asList(2, 3, 4, 5));
        Set<Integer> s3 = new HashSet<>(Arrays.asList(3, 4, 6));

        Set<Integer> common = new HashSet<>(s1);
        common.retainAll(s2);
        common.retainAll(s3);

        System.out.println(common);
    }
}
```

Solution 2: any number of sets

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        Set<Integer> s1 = new HashSet<>(Arrays.asList(1, 2, 3, 4));
        Set<Integer> s2 = new HashSet<>(Arrays.asList(2, 3, 4, 5));
        Set<Integer> s3 = new HashSet<>(Arrays.asList(3, 4, 6));

        List<Set<Integer>> sets = Arrays.asList(s1, s2, s3);

        Set<Integer> common = new HashSet<>(sets.get(0));
        for (Set<Integer> s : sets) {
            common.retainAll(s);
        }

        System.out.println(common);
    }
}
```

## Question 12: Check if two LinkedLists are equal

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        LinkedList<Integer> a = new LinkedList<>(Arrays.asList(1, 2, 3));
        LinkedList<Integer> b = new LinkedList<>(Arrays.asList(1, 2, 3));
        LinkedList<Integer> c = new LinkedList<>(Arrays.asList(3, 2, 1));

        System.out.println(a.equals(b));
        System.out.println(a.equals(c));
    }
}
```

## Question 13: Check if a HashSet is a subset of another HashSet

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        Set<Integer> big = new HashSet<>(Arrays.asList(1, 2, 3, 4));
        Set<Integer> small = new HashSet<>(Arrays.asList(2, 3));
        Set<Integer> other = new HashSet<>(Arrays.asList(2, 9));

        System.out.println(big.containsAll(small));
        System.out.println(big.containsAll(other));
    }
}
```