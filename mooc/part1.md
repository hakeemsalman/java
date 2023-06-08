# Java

## History of Java

Java is a general-purpose programming language that was originally developed by *James Gosling* and his team at Sun Microsystems in the early 1990s. The language was designed to be platform-independent, which means that code written in Java can run on any platform that has a Java Virtual Machine (JVM).

The language was initially called "Oak" because of the oak tree outside Gosling's office, but was later renamed to "Java" due to trademark issues.

Later “Oracle corp.” buys the “Sun Microsystem” in 2009


## Part 1 

### Lesson 1 - Basics - Familiar with Java Syntax

- Learn to write a program that prints text.
- Become familiar with executing programs.
- Know what the term "parameter" means.

#### Printing

```java
System.out.println("Hello World");
// The above code print(display) on the screen terminal 
```
Below is a program written with Java. What does it print?
```java
public class Example {
  public static void main(String[] args) {
    System.out.println("Welcome to the IT course - you will learn to program!");
  }
}
```
**output**
```cs
Welcome to the IT course - you will learn to program!
```

***Assignment 1***
The exercise template has the following boilerplate code:
Display your Name by using “sop” [ System.out.println(“ ”); ]
```java
public class Main{
    public static void main(String[] args) {
        // Write your program here

    }
}
```
**output**
```cs
salman
```
#### Printing Multiple Lines

```java
public class Ohjelma {
    public static void main(String[] args) {
        System.out.println("Hello world!");
        System.out.println("... and the universe!");
    }
}
```
**output**
```cs
Hello world!
… and the universe!
```
***Assignment 2***  
Q) Write a program to print a given output.
**output**
```cs
Once upon a time
there was
a program
```

#### Comments
- Single-line comments are marked with two slashes //.
- Multi-line comments are marked with a slash and an asterisk /*, and closed with an asterisk followed by a slash */

```java
public class Comments {
    public static void main(String[] args) {
        // Printing
        System.out.println("Text to print");
        System.out.println("More text to print!");
        /* Next:
        - more on printing
        - more practice
        - variables
        - ...
        */
        System.out.println("Some other text to print");
        // System.out.println("Trying stuff out")
    }
}
```

### Lesson 2 - Reading input

- Learn to write a program that reads text written by a user.
- Know what a "string" refers to in programming.
- Know how to join (i.e., "concatenate") strings together.

#### Scanner

For reading input, we use the Scanner tool that comes with Java.

```java
import java.util.Scanner;

public class Program {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // We can now use the scanner tool.
        // This tool is used to read input.
    }
}
```

**Example:-**


```java
To use the Scanner tool, we have to import the Scanner utility.

// Introduce the scanner tool used for reading user input
import java.util.Scanner;

public class Program {

    public static void main(String[] args) {
        // Create a tool for reading user input and name it scanner
        Scanner scanner = new Scanner(System.in);

        // Print "Write a message: "
        System.out.println("Write a message: ");

        // Read the string written by the user, and assign it
        // to program memory "String message = (string that was given as input)"
        String message = scanner.nextLine();

        // Print the message written by the user
        System.out.println(“Your message, ”+message);
    }
}
```
***Assignment 3***
Write a program that asks the user to write a string.
```cs
Console:
Write a message:
Bye
Bye

Write a message:
Once upon a time...
Once upon a time…
```


