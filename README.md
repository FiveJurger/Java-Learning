# Java-Learning
Bunch of code I made while trying to learn Java

## Used-Materials
Video(currently on 4th hour out fo 12) 
[https://youtu.be/xTtL8E4LzTQ?si=0ku43a4HC7b1Kx8T](url)

Book in a pdf format 
[https://www.iitk.ac.in/esc101/share/downloads/javanotes5.pdf](url)

W3Schools guides 
[https://www.w3schools.com/java/](url)


IntelliJ IDEA Community Edition 2025 
[https://www.jetbrains.com/idea/download/](url)

Java SDK - 21 Oracle OpenJDK 21.0.7
[https://www.oracle.com/java/technologies/javase/jdk21-archive-downloads.html](url)

## Code

```java
public class 〈program-name 〉 {
〈optional-variable-declarations-and-subroutines〉
public static void main(String[] args) {
〈statements 〉
}
〈optional-variable-declarations-and-subroutines〉
}
```


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

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args){

        //Scanner package used to get input from user

        Scanner input = new Scanner(System.in);

        String adjective1;
        String noun1;
        String adjective2;
        String verb1;
        String adjective3;

        System.out.print("Enter an adjective (description): ");
        adjective1 = input.nextLine();

        System.out.print("Enter a noun (animal or person): ");
        noun1 = input.nextLine();

        System.out.print("Enter an adjective (description): ");
        adjective2 = input.nextLine();

        System.out.print("Enter a verb ending with -ing (action): ");
        verb1 = input.nextLine();

        System.out.print("Enter an adjective (description): ");
        adjective3 = input.nextLine();

        System.out.println("\nToday I went to a " + adjective1 + " zoo.");
        System.out.println("In an exhibit, I saw a " + noun1 + ".");
        System.out.println(noun1 + " was " + adjective2 + " and " + verb1 + "!");
        System.out.println("I was " + adjective3 + "!");

        input.close();
    }
}
```


```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args){

        //SHOPPING CART PROGRAMME

        Scanner input = new Scanner(System.in);

        String item;
        double price;
        int quantity;
        double total;
        char currency = '$';

        System.out.print("What Item would you like to buy?: ");
        item = input.nextLine();

        System.out.print("What is the price for each?: ");
        price = input.nextDouble();

        System.out.print("How many would you like?: ");
        quantity = input.nextInt();
        input.nextLine();

        total = price * quantity;

        System.out.println("\nYou have bought " + quantity + " " + item + "/s");
        System.out.println("Your total is " + currency + total);

        input.close();
    }
}
```


```java
import java.util.Scanner;
import java.util.Random;

public class Main {
    public static void main(String[] args){

        //DICE ROLLER

        Scanner input = new Scanner(System.in);
        Random random = new Random();

        int sides;
        int result;

        System.out.print("How many sides does the dice have?: ");
        sides = input.nextInt();

        result = random.nextInt(1, sides+1);

        System.out.println("\nThe dice rolled: " + result);

        input.close();
    }
}
```


```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args){

        //COMPOUND INTEREST CALCULATOR

        Scanner input = new Scanner(System.in);

        double principal;
        double rate;
        int timesCompound;
        int years;
        char currency = '$';
        double amount;

        System.out.print("Enter the principal amount: ");
        principal = input.nextDouble();

        System.out.print("Enter the interest rate (in %): ");
        rate = input.nextDouble() / 100;

        System.out.print("Enter the # of times compound per year: ");
        timesCompound = input.nextInt();
        input.nextLine();

        System.out.print("Enter the # of years: ");
        years = input.nextInt();
        input.nextLine();

        amount = principal * Math.pow(1 + rate / timesCompound, timesCompound * years);

        System.out.printf("\nThe amount after %d years is %c%,.2f", years, currency, amount);

        input.close();

    }
}
```


```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args){

        //WEIGHT CONVERSION PROGRAMME

        Scanner input = new Scanner(System.in);

        double weight;
        double result;
        int convertChoice;

        System.out.println("Weight conversion programme");
        System.out.println("1: Convert lbs to kgs");
        System.out.println("2: Convert kgs to lbs");

        System.out.print("Choose an option: ");
        convertChoice = input.nextInt();
        input.nextLine();

        if(convertChoice == 1){
            System.out.print("\nEnter the weight in lbs: ");
            weight = input.nextDouble();

            result = weight / 2.205;
            System.out.printf("The new weight in lbs is: %.2f", result);
        }
        else if (convertChoice == 2) {
            System.out.print("\nEnter the weight in kgs: ");
            weight = input.nextDouble();

            result = weight * 2.205;
            System.out.printf("The new weight in kgs is: %.2f", result);
        }
        else{
            System.out.print("\nThe letter is invalid!");
        }

        input.close();
    }
}
```


```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args){

        //TEMPERATURE CONVERTION PROGRAMME

        Scanner input = new Scanner(System.in);

        double temperature;
        double convertedTemperature;
        String chosen;

        System.out.println("Temperature converter");

        System.out.print("\nEnter the temperature: ");
        temperature = input.nextDouble();

        System.out.print("Convert to Celsius or Fahrenheit? (C or F): ");
        chosen = input.next().toUpperCase();
        input.nextLine();

        // '?' - checks if condition is true(chosen.equals("C")), then (temperature - 32) / 1.8  else (temperature * 1.8) + 32
        
        convertedTemperature = (chosen.equals("C")) ? (temperature - 32) / 1.8 : (temperature * 1.8) + 32;
        System.out.printf("\nyour temperature is %.2f°%s", convertedTemperature, chosen);

        input.close();
    }
}
```


```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args){

        //SIMPLE CALCULATOR

        Scanner input = new Scanner(System.in);

        double firstNumber;
        char operator;
        double secondNumber;
        double result = 0;
        boolean validOperation = true;

        System.out.print("Enter the first number: ");
        firstNumber = input.nextDouble();

        System.out.print("Enter an  (+, -, *, /, ^): ");
        operator = input.next().charAt(0);

        System.out.print("Enter the second number: ");
        secondNumber = input.nextDouble();

        switch (operator){
            case '+' -> result = firstNumber + secondNumber;
            case '-' -> result = firstNumber - secondNumber;
            case '*' -> result = firstNumber * secondNumber;
            case '/' -> {
                if(secondNumber == 0){
                    System.out.println("Cannot divide by zero!");
                    validOperation = false;
                }
                else {
                    result = firstNumber / secondNumber;
                }
            }
            case '^' -> result = Math.pow(firstNumber, secondNumber);
            default -> {
                System.out.println("Invalid operator!");
                validOperation = false;
            }
        }
        if(validOperation){
            System.out.println(result);
        }

        input.close();
    }
}
```


```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args){

        // LOGICAL OPERATORS

        // && = AND  checks more than one condition. Both must be true
        // || = OR   at least one condition must be true
        // ! = NOT   checks if something is NOT true (inverse)

        // Username must be between 4-12 characters
        // Username must not contain spaces or underscores

        Scanner input = new Scanner(System.in);

        String username;

        System.out.print("Enter your new username: ");
        username = input.nextLine();

        if(username.length() < 4 || username.length() > 12){
            System.out.println("Username must be between 4-12 characters!");
        }
        else if (username.contains(" ") || username.contains("_")) {
            System.out.println("Username must not contain spaces or underscores!");
        }
        else{
            System.out.printf("Your new username is %s", username);
        }

        input.close();
    }
}
```


```java
import java.util.Random;
import java.util.Scanner;

public class Main {
    public static void main(String[] args){

        // NUMBER GUESSING GAME

        Scanner input = new Scanner(System.in);
        Random random = new Random();

        int guess;
        int attempts = 0;
        int randomNumber = random.nextInt(1, 100 + 1);

        System.out.println("Number guessing game");
        System.out.println("Guess a number between 1-100");

        do{
            System.out.print("\nEnter a guess: ");
            guess = input.nextInt();
            attempts++;

            if(guess < randomNumber){
                System.out.println("Too low! Try again.");
            }
            else if(guess > randomNumber){
                System.out.println("Too high! Try again.");
            }
            else{
                System.out.printf("Correct! The number was %d", randomNumber);
                System.out.printf("\n# of attempts: %d ", attempts);
            }

        }while(guess != randomNumber);

        System.out.println("\nYou have won!");

        input.close();
    }
}
```


```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) throws  InterruptedException{

        Scanner input = new Scanner(System.in);

        //for loop = execute some code a CERTAIN amount of times
        
        System.out.print("How many second to countdown from?: ");
        int start = input.nextInt();

        for(int i = start ; i > 0 ; i-- ){
            System.out.println(i);
            Thread.sleep(1000);
        }

        System.out.println("Happy New Year!");

        input.close();
    }
}
```
