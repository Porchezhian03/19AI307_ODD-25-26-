# Ex.No:2(B) METHODS

## QUESTION:
Write a class with one static method and one non-static method. Call both from the main() method.

When staticMethod() is called, it should print  "I am static".

When nonStaticMethod() is called, it should print  "I am non-static"

<img width="169" height="153" alt="image" src="https://github.com/user-attachments/assets/34d50995-5383-43f7-bbe8-2d0716447279" />



## AIM:
To create a Java class with one static method and one non-static method, and demonstrate calling both from the main() method.


## ALGORITHM :
1.	Start the program and define a class MyClass.

2. Create a static method staticMethod() that prints "I am static".

3. Create a non-static method nonStaticMethod() that prints "I am non-static".

4. In the main() method, call the static method directly using the class name.

5. Create an object of MyClass and call the non-static method using this object,        then stop the program.





## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by:PORCHEZHIAN E
RegisterNumber: 212224040235

*/
```

## SOURCE CODE:

```
public class MyClass {
    public static void staticMethod() {
        System.out.println("I am static");
    }
    public void nonStaticMethod() {
        System.out.println("I am non-static");
    }

    public static void main(String[] args) {
        MyClass.staticMethod();
        MyClass obj = new MyClass();
        obj.nonStaticMethod();
    }
}
```





## OUTPUT:

<img width="415" height="177" alt="image" src="https://github.com/user-attachments/assets/42d4690f-4107-4267-9fa7-b525104e3635" />


## RESULT:
The program successfully calls the static method to print “I am static” and the non-static method to print “I am non-static”.

