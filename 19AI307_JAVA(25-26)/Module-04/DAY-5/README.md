# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:

Create a program that sends different types of notifications: "email", "sms", and "push". Use the Factory Pattern to generate the appropriate notification sender and call its notifyUser() method.

## AIM:

To implement the Factory Design Pattern to send different types of notifications — Email, SMS, and Push.

## ALGORITHM :
1. Start the program.

2. Import the necessary package 'java.util'

3. Create a Notification interface with the method notifyUser().

4. Implement this interface in classes EmailNotification, SMSNotification, and PushNotification.

5. Create a NotificationFactory class to generate objects based on input type.

6. In main(), read the notification type and get the corresponding object from the factory.

7. Call the notifyUser() method to send the notification.




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

interface Notification {
   void notifyUser();
}

class EmailNotification implements Notification {
   public void notifyUser() {
       System.out.println("Sending Email Notification");
   }
}

class SMSNotification implements Notification {
   public void notifyUser() {
       System.out.println("Sending SMS Notification");
   }
}

class PushNotification implements Notification {
   public void notifyUser() {
       System.out.println("Sending Push Notification");
   }
}

class NotificationFactory {
   public Notification createNotification(String type) {
       switch(type.toLowerCase()) {
           case "email": return new EmailNotification();
           case "sms": return new SMSNotification();
           case "push": return new PushNotification();
           default: return null;
       }
   }
}

public class Main {
   public static void main(String[] args) {
       Scanner sc = new Scanner(System.in);
       NotificationFactory factory = new NotificationFactory();
       
       while(true) {
           String input = sc.nextLine();
           if(input.equalsIgnoreCase("exit")) break;

           Notification notification = factory.createNotification(input);
           if(notification != null) {
               notification.notifyUser();
           } else {
               System.out.println("Invalid notification type: " + input);
           }
       }

       sc.close();
   }
}
```





## OUTPUT:

<img width="1284" height="374" alt="512464944-ea1d8e4c-e2a0-40dc-ac41-02cd410c4c07" src="https://github.com/user-attachments/assets/e5cd394c-3105-498c-be95-052072fb7ea8" />


## RESULT:

The program successfully creates and sends the appropriate type of notification using the Factory Pattern.
