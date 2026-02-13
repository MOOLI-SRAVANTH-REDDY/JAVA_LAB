
## EXPERIMENT 4A
## TITLE:SINGLE INHERITANCE
```java
class Person
{
String name;
int age;
Person(String name,int age)
{
this.name=name;
this.age=age;
}
void displayPersonDetails()
{
  System.out.println("name:"+name);
  System.out.println("Age:"+age);
}
}
class Employee extends Person {
    double annualSalary;
    int yearOfJoining;
    String nationalInsuranceNumber;

    Employee(String name, int age, double annualSalary, int yearOfJoining, String nationalInsuranceNumber) {
        super(name, age);
        this.annualSalary = annualSalary;
        this.yearOfJoining = yearOfJoining;
        this.nationalInsuranceNumber = nationalInsuranceNumber;
    }

    void displayEmployeeDetails() {
        displayPersonDetails();
        System.out.println("Annual Salary : " + annualSalary);
        System.out.println("Year Of Joining : " + yearOfJoining);
        System.out.println("National Insurance Number : " + nationalInsuranceNumber);
    }
}
public class TestEmployee {
    public static void main(String[] args) {
        Employee emp1 = new Employee("Rahul", 28, 550000, 2021, "NI12345A");
        Employee emp2=  new Employee("ram",29,560000,2022,"NI12345B");
        emp1.displayEmployeeDetails();
        emp2.displayEmployeeDetails();
    }
}

```
## OUTPUT

![output of main method](singleInheritance.png)






## EXPERIMENT 4B

## TITLE:MULTI LEVEL INHERITANCE

```java

class Bicycle {
    String pedalType;

    void showBicycleInfo() {
        System.out.println("This is a bicycle with pedals.");
    }
}
class Motorbike extends Bicycle {
    int engineCapacity;

    void showMotorbikeInfo() {
        System.out.println("This motorbike has an engine.");
    }
}
class ElectricBike extends Motorbike {
    int batteryCapacity;

    void showElectricBikeInfo() {
        System.out.println("This electric bike has an electric motor and battery.");
    }
}
public class TestVehicle {
    public static void main(String[] args) {
        ElectricBike eBike = new ElectricBike();

        eBike.pedalType = "Standard Pedals";
        eBike.engineCapacity = 250;
        eBike.batteryCapacity = 500;

        eBike.showBicycleInfo();
        eBike.showMotorbikeInfo();
        eBike.showElectricBikeInfo();
    }
}


```

## OUTPUT




![output](multilevel.png)


## EXPERIMENT 4C
## TITLE: ABSTRACT

```java

##abstract Class:
public abstract class Figure {
    double dim1;
    double dim2;

    Figure(double dim1, double dim2) {
        this.dim1 = dim1;
        this.dim2 = dim2;
    }


    abstract double area();
}


public class Rectangle extends Figure {

    public Rectangle(double length, double breadth) {
        super(length, breadth);
    }

    double area() {
        return dim1 * dim2;
    }
}


public class Triangle extends Figure {


    Triangle(double base, double height) {
        super(base, height);
    }


    double area() {
        return 0.5 * dim1 * dim2;
    }
}
public class TestFigure {
    public static void main(String[] args) {

        Figure f1 = new Rectangle(10, 5);
        System.out.println("Area of Rectangle = " + f1.area());

        Figure f2 = new Triangle(8, 6);
        System.out.println("Area of Triangle = " + f2.area());
    }
}

```

## OUTPUT
![ouput](Abstract.png)

