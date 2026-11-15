# Java Collections: Stack

## Question 26: Implement a Stack using the Stack class

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        Stack<Integer> stack = new Stack<>();
        stack.push(1);
        stack.push(2);
        stack.push(3);

        System.out.println(stack.peek());
        System.out.println(stack.pop());
        System.out.println(stack.isEmpty());
    }
}
```

## Question 27: Implement a Stack using the LinkedList class

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

## Question 28: Implement a Stack using the ArrayDeque class

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        Deque<Integer> stack = new ArrayDeque<>();
        stack.push(1);
        stack.push(2);
        stack.push(3);

        System.out.println(stack.peek());
        System.out.println(stack.pop());
        System.out.println(stack.isEmpty());
    }
}
```

## Question 29: Implement a Stack using PriorityQueue with a custom comparator

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
