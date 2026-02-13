## EXPERIMENT 5A
## TITLE:INTERFACE
```java

interface Sortable {
    void sort(int[] arr);
}
class BubbleSort implements Sortable {

    public void sort(int[] arr) {

        int n = arr.length;
        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - i - 1; j++) {

                if (arr[j] > arr[j + 1]) {

                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }
    }
}
class SelectionSort implements Sortable {

    public void sort(int[] arr) {

        int n = arr.length;
        for (int i = 0; i < n - 1; i++) {
            int minIndex = i;
            for (int j = i + 1; j < n; j++) {

                if (arr[j] < arr[minIndex]) {
                    minIndex = j;
                }
            }

            int temp = arr[minIndex];
            arr[minIndex] = arr[i];
            arr[i] = temp;
        }
    }
}
public class TestSort {

    public static void main(String[] args) {
        int[] arr1 = {5, 3, 8, 1, 2};
        Sortable ref;

        ref = new BubbleSort();
        ref.sort(arr1);

        System.out.println("Array sorted using BubbleSort:");
        for (int i = 0; i < arr1.length; i++) {
            System.out.print(arr1[i] + " ");
        }

        System.out.println();
        int[] arr2 = {9, 4, 7, 2, 6};

        ref = new SelectionSort();
        ref.sort(arr2);

        System.out.println("Array sorted using SelectionSort:");
        for (int i = 0; i < arr2.length; i++) {
            System.out.print(arr2[i] + " ");
        }
    }
}
```


## OUTPUT
![output](Interface.png)




## EXPERIMENT 5B
## TITLE:POLYMORPHISM
```java
class Vehicle {
    void run() {
        System.out.println("Vehicle is running");
    }
}
class Car extends Vehicle {
    void run() {
        System.out.println("Car is running on four wheels");
    }
}
class Bike extends Vehicle {
    void run() {
        System.out.println("Bike is running on two wheels");
    }
}
public class TestVehicle {
    public static void main(String[] args) {

        Vehicle v;

        v = new Car();
        v.run();

        v = new Bike();
        v.run();

        v = new Vehicle();
        v.run();
    }
}

```
## OUTPUT
![output](Polymorphism.png)









## EXPERIMENT 5C

## TITLE:STRINGBUFFER

```java
public class DeleteStringBuffer {
   public DeleteStringBuffer() {
   }

   public static void main(String[] var0) {
      StringBuffer var1 = new StringBuffer("Java Programming");
      System.out.println("Original String: " + String.valueOf(var1));
      var1.deleteCharAt(4);
      System.out.println("After deleting character at index 4: " + String.valueOf(var1));
      var1.delete(0, 4);
      System.out.println("After deleting range (0 to 4): " + String.valueOf(var1));
   }
}

```
## OUTPUT

![ouput](StringBuffer.png)

