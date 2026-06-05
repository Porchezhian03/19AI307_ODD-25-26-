# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:

You wrote a program that stores some input strings into a String array and prints each string in uppercase. However, you're getting a NullPointerException. What should you check in your array before calling .toUpperCase() on a element?

## AIM:

To handle a NullPointerException when performing operations on a null string in Java.

## ALGORITHM :
1. Start the program.

2. Import the necessary package 'java.util'

3. Read a string input from the user.

4. If the input is "null", assign null to the variable.

5. Try converting the string to uppercase using toUpperCase().

6. Catch and handle the NullPointerException if the string is null.

7. Print "Null element" in case of exception.





## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: PORCHEZHIAN E
RegisterNumber: 212224040235
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class NullPointerArrayExample {
   public static void main(String[] args) {
       Scanner sc = new Scanner(System.in);

       String input = sc.next();
       String str = input.equalsIgnoreCase("null") ? null : input;

       try {
           System.out.println(str.toUpperCase());
       } catch (NullPointerException e) {
           System.out.println("Null element");
       }

       sc.close();
   }
}
```






## OUTPUT:

<img width="1266" height="354" alt="512459957-ca3d287f-7bcc-4852-9515-a3ff25df30a1" src="https://github.com/user-attachments/assets/edba0eb2-c06b-42f3-91d9-dd8f6ef4a7e1" />


## RESULT:

The program successfully detects and handles NullPointerException by displaying "Null element" when the input is null.
