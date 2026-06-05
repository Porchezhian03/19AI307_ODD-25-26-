# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:

Write a Java program to write characters to a file using FileWriter.

## AIM:

To write character data into a file using the FileWriter class in Java.

## ALGORITHM :

1. Start the program.

2. Import the necessary package 'java.util'

3. Import java.io.FileWriter and java.io.IOException.

4. Take user input using Scanner.

5. Create a FileWriter object with the desired file name.

6. Use write() method to write text into the file.

7. Close the FileWriter and handle exceptions using try-catch.



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

import java.io.*;

public class FileWriteExample {
   public static void main(String[] args) {
       try {
           BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
           String filename = br.readLine();
           String content = br.readLine();

           FileWriter fw = new FileWriter(filename);
           fw.write(content);
           fw.close();

           System.out.println("File written successfully.");
       } catch (IOException e) {
           System.out.println("An error occurred.");
       }
   }
}
```




## OUTPUT:

<img width="1239" height="395" alt="512468454-f1eb5219-05ab-4882-990c-ab044ebd6ca8" src="https://github.com/user-attachments/assets/ee1e13bc-7e33-4296-be0c-a24f3ceb56de" />


## RESULT:

The program successfully writes the entered text into output.txt using FileWriter.
