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

```
