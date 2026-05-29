# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a program to access a static variable using both class name and object.

<img width="398" height="150" alt="image" src="https://github.com/user-attachments/assets/a94bfbdb-d244-4bc5-9009-f9317c705905" />

## AIM:
To write a Java program that demonstrates accessing a static variable using both the class name and an object of the class.



## ALGORITHM :
1. Start the program and declare a static variable num inside the class prog.

2. In the main() method, read an integer value from the user and assign it to the       static variable num.

3. Access and print the static variable using the class name (prog.num).

4. Create an object of the class (prog obj = new prog();) and access the static         variable using the object (obj.num).

5. Stop the program after displaying the values.





## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: PORCHEZHIAN E
RegisterNumber: 212224040235
*/
```

## SOURCE CODE:


```
import java.util.Scanner;

class prog {
    
    static int num;

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        num = sc.nextInt();
        System.out.println("Accessing using class name: " + prog.num);

        prog obj = new prog();
        System.out.println("Accessing using object: " + obj.num);

        sc.close();
    }
}

```




## OUTPUT:

<img width="797" height="299" alt="image" src="https://github.com/user-attachments/assets/cc80b0ff-cc27-468a-b2b4-78749a686014" />


## RESULT:
The program successfully shows that a static variable can be accessed directly via the class name and also through an object, producing the same value.

