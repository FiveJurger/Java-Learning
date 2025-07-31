# Java-Learning
Bunch of code I made while trying to learn Java

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args){
        Scanner input = new Scanner(System.in);

        System.out.print("Enter your name: ");
        String name = input.nextLine();

        System.out.print("Enter your age: ");
        int age = input.nextInt();
        input.nextLine();

        System.out.print("What is your gpa: ");
        double gpa = input.nextDouble();

        System.out.println("Are you a student? (true/false): ");
        boolean isStudent = input.nextBoolean();

        System.out.println("Your name is: " + name);
        System.out.println("You are " + age + " years old");
        System.out.println("Your gpa is: " + gpa);
        if(isStudent){
            System.out.println(name + " is enrolled as a student");
        }
        else{
            System.out.println(name + " is not enrolled as a student");
        }

        input.close();
    }
}
```
