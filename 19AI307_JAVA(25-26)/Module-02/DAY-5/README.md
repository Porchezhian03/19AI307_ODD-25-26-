# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Calculator with: One non-static method add(int a, int b) that returns the sum, One static method info() that says "Calculator is ready".

<img width="366" height="184" alt="image" src="https://github.com/user-attachments/assets/36a7fca3-e38d-4e39-a418-cebbea122170" />



## AIM:
Create a Calculator class with a non-static add() method to sum two numbers and a static info() method to display a message.


## ALGORITHM :
1.	Start and import Scanner to read input.

2. Define Calculator class with a non-static add(a, b) method and a static info()      method.

3. Read two integers from the user using Scanner.

4. Call Calculator.info() and use a Calculator object to calculate the sum with         add(a, b).

5. Display the sum and end the program.





## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: PORCHEZHIAN E
RegisterNumber: 212224040235
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class Calculator {
    
    public int add(int a, int b) {
        return a + b;
    }

    public static void info() {
        System.out.println("Calculator is ready");
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt();
        int b = sc.nextInt();

        Calculator.info();

        Calculator calc = new Calculator();
        int sum = calc.add(a, b);

        System.out.println("Sum: " + sum);

        sc.close();
    }
}
```





## OUTPUT:

<img width="576" height="291" alt="image" src="https://github.com/user-attachments/assets/7948428a-1883-4a4c-935e-70ba499028db" />


## RESULT:
The program displays "Calculator is ready", takes two numbers as input, and then shows their sum.

