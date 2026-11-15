# Java Collections: TreeSet

## Question 43: Create a TreeSet, add elements, print in sorted order

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        Set<Integer> set = new TreeSet<>();
        set.add(2);
        set.add(3);
        set.add(1);

        System.out.println(set);
    }
}
```

## Question 44: Create a TreeSet of custom objects implementing Comparable

```java
import java.util.*;

class Student implements Comparable<Student> {
    int id;
    String name;

    Student(int id, String name) {
        this.id = id;
        this.name = name;
    }

    public int compareTo(Student o) {
        if (this.id != o.id) return this.id - o.id;
        return this.name.compareTo(o.name);
    }
}

class Main {
    public static void main(String[] args) {
        Set<Student> set = new TreeSet<>();
        set.add(new Student(3, "Riya"));
        set.add(new Student(1, "Aman"));
        set.add(new Student(1, "Zara"));
        set.add(new Student(2, "Kabir"));

        for (Student s : set) {
            System.out.println(s.id + " " + s.name);
        }
    }
}
```
