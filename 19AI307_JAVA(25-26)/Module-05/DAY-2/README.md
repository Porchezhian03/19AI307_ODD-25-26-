# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:

Write a Java program to read a string from the user, compress it in memory using ByteArrayOutputStream + GZIPOutputStream, and then decompress it back using ByteArrayInputStream + GZIPInputStream.



## AIM:

To demonstrate string compression and decompression using ByteArrayOutputStream, GZIPOutputStream, ByteArrayInputStream, and GZIPInputStream.

## ALGORITHM :
1. Start the program.

2. Import the necessary package 'java.util'

3. Read a string from the user.

4. Create a ByteArrayOutputStream and wrap it in a GZIPOutputStream to compress the string.

5. Convert the compressed output to a byte array.

6. Use ByteArrayInputStream and GZIPInputStream to decompress the byte array back to the original string.

7. Display both compressed size and decompressed string.



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
import java.util.Scanner;
import java.util.zip.GZIPOutputStream;
import java.util.zip.GZIPInputStream;

public class GZIPMemoryExample {
   public static void main(String[] args) {
       Scanner scanner = new Scanner(System.in);

       try {
           // Get input string from user
           String input = scanner.nextLine();

           // --- Compress the string ---
           ByteArrayOutputStream baos = new ByteArrayOutputStream();
           GZIPOutputStream gzipOut = new GZIPOutputStream(baos);
           gzipOut.write(input.getBytes("UTF-8"));
           gzipOut.close(); // Finish compression

           byte[] compressedData = baos.toByteArray();
           System.out.println("Compressed data (bytes):");
           for (byte b : compressedData) {
               System.out.print(b + " ");
           }
           System.out.println("\nTotal bytes: " + compressedData.length);

           // --- Decompress the string ---
           ByteArrayInputStream bais = new ByteArrayInputStream(compressedData);
           GZIPInputStream gzipIn = new GZIPInputStream(bais);
           InputStreamReader reader = new InputStreamReader(gzipIn, "UTF-8");
           BufferedReader br = new BufferedReader(reader);

           StringBuilder decompressed = new StringBuilder();
           String line;
           while ((line = br.readLine()) != null) {
               decompressed.append(line);
           }

           System.out.println("\nDecompressed string:");
           System.out.println(decompressed.toString());

       } catch (IOException e) {
           System.out.println("Error: " + e.getMessage());
       }

       scanner.close();
   }
}
```





## OUTPUT:

<img width="1271" height="577" alt="512470657-ec980f76-7dcd-46aa-8c14-33fe5d578589" src="https://github.com/user-attachments/assets/a836c1f5-57db-491d-b244-31a6b3dc88f8" />


## RESULT:

The program successfully compresses and decompresses a string in memory using GZIP streams, showing reduced data size and restoring the original text accurately.
