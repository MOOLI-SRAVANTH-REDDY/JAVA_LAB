## EXPERIMEMT 6A
## TITLE: EXCEPTION HANDLING
``` java
import java.util.Scanner;

public class ExceptionArray {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter size of array: ");
        int n = sc.nextInt();

        int[] arr = new int[n];

        for (int i = 0; i < n; i++) {
            System.out.print("Enter element at index " + i + ": ");
            arr[i] = sc.nextInt();
        }

        System.out.print("Enter index to access: ");
        int index = sc.nextInt();

        try {
            System.out.println("Element at index " + index + " is: " + arr[index]);
        } 
        catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Invalid index! Please enter index between 0 and " + (n - 1));
        }

        sc.close();
    }
}

```


## OUTPUT

![output](.png)
