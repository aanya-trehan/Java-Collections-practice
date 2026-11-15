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
import java.util.*;

class Main {
    public static void main(String[] args) {
        Queue<Integer> q = new LinkedList<>();
        q.add(10);
        q.add(20);
        q.add(30);

        System.out.println(q.peek());
        System.out.println(q.poll());
        System.out.println(q);
    }
}
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
