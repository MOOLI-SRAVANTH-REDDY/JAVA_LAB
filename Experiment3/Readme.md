
## EXPERIMENT3(A)

## TITLE:CONSTRUCTOR OVERLOADING
```java
class Student1 { 
String name; int age; int marks;
 Student1()
 {
        name = "Not Assigned";
        age = 0;
        marks = 0;
    }
    Student1(String n, int a) {
        name = n;
        age = a;
        marks = 0;
    }
    Student1(String n, int a, int m) {
        name = n;
        age = a;
        marks = m;
    }
    void display() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Marks: " + marks);
    }
}
public class Student1Main {
    public static void main(String[] args) {
        Student1 s1 = new Student1();
        Student1 s2 = new Student1("Alice", 20);
        Student1 s3 = new Student1("Bob", 22, 90);

        s1.display();
        s2.display();
        s3.display();
    }

}

```


## OUTPUT 



![output of main method](Constructor.png)

