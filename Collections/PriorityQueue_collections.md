# Java Collections: PriorityQueue

## Question 20: Add elements to a PriorityQueue and print them in sorted order

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        PriorityQueue<Integer> pq = new PriorityQueue<>();
        pq.add(30);
        pq.add(10);
        pq.add(50);
        pq.add(20);

        while (!pq.isEmpty()) {
            System.out.print(pq.poll() + " ");
        }
    }
}
```

## Question 21: Implement a priority queue using the PriorityQueue class

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        PriorityQueue<Integer> pq = new PriorityQueue<>();

        pq.add(5);
        pq.add(1);
        pq.add(3);

        System.out.println(pq.peek());
        System.out.println(pq.poll());
        System.out.println(pq.size());
        System.out.println(pq.contains(3));
        pq.remove(3);
        System.out.println(pq.isEmpty());
    }
}
```

## Question 22: Implement a priority queue using a custom comparator

Solution 1: biggest first

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        PriorityQueue<Integer> pq = new PriorityQueue<>(Collections.reverseOrder());
        pq.add(30);
        pq.add(10);
        pq.add(50);

        while (!pq.isEmpty()) {
            System.out.print(pq.poll() + " ");
        }
    }
}
```

Solution 2: custom objects

```java
import java.util.*;

class Task {
    String name;
    int priority;

    Task(String name, int priority) {
        this.name = name;
        this.priority = priority;
    }
}

class Main {
    public static void main(String[] args) {
        PriorityQueue<Task> pq = new PriorityQueue<>(
            (a, b) -> Integer.compare(a.priority, b.priority));

        pq.add(new Task("write report", 3));
        pq.add(new Task("fix bug", 1));
        pq.add(new Task("reply email", 2));

        while (!pq.isEmpty()) {
            System.out.println(pq.poll().name);
        }
    }
}
```

## Question 23: Implement a PriorityQueue using a custom comparator

Shortest word first, and alphabetical when the lengths are equal.

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        PriorityQueue<String> pq = new PriorityQueue<>((a, b) -> {
            if (a.length() != b.length()) {
                return Integer.compare(a.length(), b.length());
            }
            return a.compareTo(b);
        });

        pq.add("banana");
        pq.add("fig");
        pq.add("apple");
        pq.add("kiwi");
        pq.add("pear");

        while (!pq.isEmpty()) {
            System.out.print(pq.poll() + " ");
        }
    }
}
```

## Question 24: Implement a Queue using PriorityQueue with a custom comparator

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

## Question 25: Implement a Stack using PriorityQueue with a custom comparator

```java
import java.util.*;

class MyStack {
    private static class Item {
        int value;
        int order;
        Item(int value, int order) {
            this.value = value;
            this.order = order;
        }
    }

    private PriorityQueue<Item> pq =
        new PriorityQueue<>((a, b) -> Integer.compare(b.order, a.order));
    private int counter = 0;

    void push(int x)  { pq.add(new Item(x, counter++)); }
    int pop()         { return pq.poll().value; }
    int peek()        { return pq.peek().value; }
    boolean isEmpty() { return pq.isEmpty(); }
}

class Main {
    public static void main(String[] args) {
        MyStack s = new MyStack();
        s.push(30);
        s.push(10);
        s.push(20);

        while (!s.isEmpty()) {
            System.out.print(s.pop() + " ");
        }
    }
}
```
