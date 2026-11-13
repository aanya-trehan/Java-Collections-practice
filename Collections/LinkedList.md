# Java Collections: LinkedList

## Question 34: Create a LinkedList and perform add, remove, and iterate

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        LinkedList<Integer> ll = new LinkedList<>();
        ll.add(1);
        ll.add(2);
        ll.add(3);

        ll.remove();
        ll.remove(Integer.valueOf(2));

        ll.add(2);
        ll.add(3);

        for (Integer item : ll) {
            System.out.println(item);
        }
    }
}
```

## Question 35: Implement a Queue using the LinkedList class

```java

```

## Question 36: Implement a Stack using the LinkedList class

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        LinkedList<Integer> stack = new LinkedList<>();
        stack.add(1);
        stack.add(2);
        stack.add(3);

        System.out.println(stack.peekLast());
        System.out.println(stack.removeLast());
        System.out.println(stack.isEmpty());
    }
}
```

## Question 37: Check if two LinkedLists are equal

```java

```
