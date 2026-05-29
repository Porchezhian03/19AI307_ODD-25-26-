# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java Program to Find the Average of Array Elements.

<img width="464" height="266" alt="image" src="https://github.com/user-attachments/assets/f581508f-da33-4d60-835b-63d39aca3e32" />


## AIM:
To write a Java program that calculates the average of elements in an array.


## ALGORITHM :
1. Start the program and read the number of elements n from the user.

2. Create an array of size n and read n integer elements from the user into the array.

3. Initialize a variable sum to 0 and add all array elements to sum using a loop.

4. Calculate the average by dividing sum by n and store it in a double variable.

5. Display the average value and stop the program.





## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: PORCHEZHIAN E
RegisterNumber: 212224040235

*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class AverageArray {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = scanner.nextInt();
        }
        scanner.close();
        int sum = 0;
        for (int num : arr) {
            sum += num;
        }
        double average = (double) sum / n;
        System.out.printf("The average of elements is %.2f\n", average);
    }
}

```





## OUTPUT:

<img width="794" height="472" alt="image" src="https://github.com/user-attachments/assets/d9d45b19-9d58-49a4-a6c4-50b7c17264ec" />


## RESULT:
The program successfully computes and displays the average value of all the array elements entered by the user.




