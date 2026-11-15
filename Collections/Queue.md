# Java Collections: Queue

## Question 38: Implement a Queue using the LinkedList class

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

## Question 39: Implement a priority queue using a custom comparator

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        Queue<Integer> q = new PriorityQueue<>((a, b) -> b - a);
        q.add(30);
        q.add(10);
        q.add(20);

        while (!q.isEmpty()) {
            System.out.print(q.poll() + " ");
        }
    }
}
```

## Question 40: Implement a Queue using the PriorityQueue class

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        Queue<Integer> q = new PriorityQueue<>();
        q.add(30);
        q.add(10);
        q.add(20);

        System.out.println(q.peek());
        while (!q.isEmpty()) {
            System.out.print(q.poll() + " ");
        }
    }
}
```

## Question 41: Implement a Queue using the ArrayDeque class

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        Queue<Integer> q = new ArrayDeque<>();
        q.add(10);
        q.add(20);
        q.add(30);

        System.out.println(q.peek());
        System.out.println(q.poll());
        System.out.println(q);
    }
}
```

## Question 42: Implement a Queue using PriorityQueue with a custom comparator

```java
import java.util.*;

class MyQueue {
    private static class Item {
        int value;
        int order;
        Item(int value, int order) {
            this.value = value;
            this.order = order;
        }
    }

    private PriorityQueue<Item> pq =
        new PriorityQueue<>((a, b) -> Integer.compare(a.order, b.order));
    private int counter = 0;

    void enqueue(int x) { pq.add(new Item(x, counter++)); }

    int dequeue()       { return pq.poll().value; }

    int front()         { return pq.peek().value; }

    boolean isEmpty()   { return pq.isEmpty(); }
}

class Main {
    public static void main(String[] args) {
        MyQueue q = new MyQueue();
        q.enqueue(30);
        q.enqueue(10);
        q.enqueue(20);

        while (!q.isEmpty()) {
            System.out.print(q.dequeue() + " ");
        }
    }
}
```
