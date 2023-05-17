# Problems

## List of Problems
--------------------------
1. [Prime Number](#prime-number-check)
2. [Leay Year](#leap-year)
3. [Find the Largest number](#find-the-largest-number)
4. [Check letter is Upper or Lower case](#check-letter-is-upper-or-lower-case)
5. [Fibonacci number](#fibonacci-number)
6. [Counting Occurances](#counting-occurances)
7. [Reverse](#reverse)
8. [Swap Two Numbers](#swap-two-numbers)
9. [ArmStrong Numbers](#armstrong-numbers)

## Basics 
----------------
1. [Write a program to print whether a number is even or odd, also take input from the user.](write-a-program-to-print-whether-a-number-is-even-or-odd,-also-take-input-from-the-user.)
2. [Take name as input and print a greeting message for that particular name.](take-name-as-input-and-print-a-greeting-message-for-that-particular-name.)
3. Write a program to input principal, time, and rate (P, T, R) from the user and find Simple Interest.
4. Take in two numbers and an operator (+, -, *, /) and calculate the value. (Use if conditions)
5. Take 2 numbers as input and print the largest number.
6. Input currency in rupees and output in USD.
7. To calculate Fibonacci Series up to n numbers.
8. To find out whether the given String is Palindrome or not.
9. To find Armstrong Number between two given number.

## Prime Number Check
```java
static boolean isPrime(int n)
    {
        // Corner case
        if (n <= 1)
            return false;

        // Check from 2 to n-1
        for (int i = 2; i < n; i++)
            if (n % i == 0)
                return false;

        return true;
    }
```
Another method
```java
public class Main(){
    public static void main(Strings[] args)
    {
        Scanner scan = new Scanner(System.in);
        int num1 = scan.nextInt();

       System.out.println(isPrime(num1));

    }
    static boolean isPrime(n){
        if(n <= 1){
            return false;
        }
        int c =2;
        while(c * c <= n){
            if(n % c == 0){
                return false;
            }
            c++;
        }
        return c * c > n;
    }
}
```

---

## Leap Year

```java
 int x=1800;
      if(x % 4 ==0){
          System.out.print("Leap year " + x);
      } else if(x % 100 == 0 && x % 400 == 0){
          System.out.print("Leap year " + x);

      } else           System.out.print("Not a Leap year " + x);

    }
```

the above code DOES NOT work properly.

```java
 if ((year % 400 == 0) || ((year % 4 == 0) && (year % 100 != 0))) {
    // Both conditions true- Print leap year
       System.out.println(year + " : Leap Year");
  } else {
    // Any condition fails- Print Non-leap year
      System.out.println(year + " : Non - Leap Year");
  }
```

This above code works properly :smile:

---

## Find the Largest number

```java
public class Main{
    public static void main(Strings[] args)
    {
        Scanner scan = new Scanner(System.in);
        int value1 = scan.nextInt();
        int value2 = scan.nextInt();
        int value3 = scan.nextInt();
        int max = value1;
        if(value2 > max){
           max = value2;
        }
        if(value3 > max){
            max = value3;
        }
        System.out.print(max);
    }
}
```
---

## Check letter is Upper or Lower case

```java
public class Main(){
    public static void main(Strings[] args)
    {
        Scanner scan = new Scanner(System.in);
        char ch = scan.next();
        if(ch >= 'a' && ch <= 'z' ){
            System.out.println("lower case");
        } else{
            System.out.println("Upper case");
        }
    }
}
```
---

## Fibonacci number

```java
public class Main(){
    public static void main(Strings[] args)
    {
        Scanner scan = new Scanner(System.in);
        System.out.println("Please enter the nth number");
        int n = scan.next();
        int a = o,b = 1,c = 1;
        int count = 2;
        if(n == a){
            System.out.println(n+"th is "+a);
        } else if(n == b){
            System.out.println(n+"th is "+b);
        }else {
            while(count<=n){
            c = b + a;
            a = b;
            b = c;
            count++;
            }
            System.out.println(n+"th is "+c);
        }
    }
}
```
---

## Counting Occurances

```java
public class Main(){
    public static void main(Strings[] args)
    {
        Scanner scan = new Scanner(System.in);
        // suppose n =  12375674987

        // find the repeating number from above number,like suppose 7 is repeating number and count is 3
        int n = scan.nextInt();
        int count = 0;
        while(n>0){
            rem = n % 10;
            if(rem == 7){
                count++;
            }
            n/=10;
        }
        System.out.println(count);
    }
}
```
---

## Reverse

```java
public class Main(){
    public static void main(Strings[] args)
    {
        Scanner scan = new Scanner(System.in);
        int n = scan.nextInt();
        int rev = 0;
        while(n>0){
            int temp = n % 10;
            rev = rev * 10+temp;
            n = n/10;
        }
        System.out.println(rev);
    }
}
```

---
## Swap two numbers

```java
public class Main(){
    public static void main(Strings[] args)
    {
        Scanner scan = new Scanner(System.in);
        int num1 = scan.nextInt();
        int num2 = scan.nextInt();

        System.out.println(num1 +" and "+num2);
        int temp = num1;
        num1 = num2;
        num2 = temp;

        System.out.println(num1+" and "+num2)
    }
}
```
---
## ArmStrong Numbers

suppose a number is 153 then split individual and cube each number and then add it with others. if the result number is same then it is armstrong number.

`int a = 153;` 1<sup>3</sup> `+` 5<sup>3</sup> `+` 3<sup>3</sup>  
then `1 + 125 + 27 = 153`  
both are same then it is Armstrong number.  
examples are 3 digit arm strong number,` 153, 370, 371, 407`

```java
public class Main(){
    public static void main(Strings[] args)
    {
        Scanner scan = new Scanner(System.in);
        int num1 = scan.nextInt();

        System.out.println(isArmStrong(num1));
    }
    static boolean isArmStrong(int n){
        int original = n
        int sum = 0;

        while(n > 0){
            int rem = n % 10;
            n = n / 10;
            sum = sum + rem*rem*rem;
        }
        if(sum == original){
            return true;
        } else return false;
    }
}
```
---
## Find max value in Array
```java
public class Max {
    public static void main(String[] args) {
        int[] arr = {1, 3, 2, 9, 18};
        System.out.println(maxRange(arr, 1, 3));
    }

    // work on edge cases here, like array being null
    static int maxRange(int[] arr, int start, int end) {

        if (start > end) {
            return -1;
        }

        if (arr == null) {
            return -1;
        }

        int maxVal = arr[start];
        for (int i = start; i <= end; i++) {
            if (arr[i] > maxVal) {
                maxVal = arr[i];
            }
        }
        return maxVal;
    }

    static int max(int[] arr) {
        if (arr.length == 0) {
            return -1;
        }
        int maxVal = arr[0];
        for (int i = 1; i < arr.length; i++) {
            if (arr[i] > maxVal) {
                maxVal = arr[i];
            }
        }
        return maxVal;
    }
}
```
## Swap values in Array
```java
import java.util.Arrays;

public class Swap {
    public static void main(String[] args) {
        int[] arr = {1, 3, 23, 9, 18, 56};
//        swap(arr, 0, 4);
        reverse(arr);
        System.out.println(Arrays.toString(arr));
    }

    static void reverse(int[] arr) {
        int start = 0;
        int end = arr.length-1;

        while (start < end) {
            // swap
            swap(arr, start, end);
            start++;
            end--;
        }
    }
    static void swap(int[] arr, int index1, int index2) {
        int temp = arr[index1];
        arr[index1] = arr[index2];
        arr[index2] = temp;
    }
}
```

# 02. First Java

## 1. Write a program to print whether a number is even or odd, also take input from the user.

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args){
        Scanner input = new Scanner(System.in);
        int number = input.nextInt();
        String ans = checkNumber(number);
        System.out.println(ans);
    }
    static String checkNumber(int a){
        if(a % 2 ==0) return "Even";
        else return "Odd";
    }
}
```
## 2. Take name as input and print a greeting message for that particular name.
```java

import java.util.Scanner;

public class GreetMessage {
    public static void main(String[] args) {
        System.out.println("Hello "+ Greet());
    }
    static String Greet(){
        Scanner input = new Scanner(System.in);
        return input.next();
    }
}
```

## 3. Write a program to input principal, time, and rate (P, T, R) from the user and find Simple Interest.
```java
import java.util.Scanner;

public class SimpleInterest {
    public static void main(String[] args) {
        System.out.println(si());
    }

    static int si() {
        Scanner input = new Scanner(System.in);
        int p = input.nextInt(), t = input.nextInt(), r = input.nextInt();
        return (p * t * r)/100;
    }
}
```

## 4. Take in two numbers and an operator (+, -, *, /) and calculate the value. (Use if conditions)
```java
import java.util.Scanner;

public class calculate {
    public static void main(String[] args) {

       System.out.println(calculator());
    }
    static int calculator(){
        Scanner input = new Scanner(System.in);
        int num1 = input.nextInt(), num2 = input.nextInt();
        String ch = input.next();
        if(ch.equals("+")){
            return num1 + num2;
        } else if(ch.equals("-")){
            return num1 - num2;
        } else if(ch.equals("*")){
            return num1 * num2;
        } else if (ch.equals("/")){
            return num1 / num2;
        } else
            return -001;
    }
}
```
## 5. Take 2 numbers as input and print the largest number.
```java
import java.util.Scanner;

public class largestNumber {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        int num1 = input.nextInt(), num2 = input.nextInt();
        System.out.println(largest(num1 , num2));
    }
    static int largest(int a, int b){
       int  max = a;
       if(b>a){
           return max = b;
       }
       return max;
    }
}
```
## 6. Input currency in rupees and output in USD.
```java
import java.util.Scanner;

public class convertCurrency {
    public static void main(String[] args) {
        System.out.println(convertor());
    }
    static double convertor(){
        Scanner input = new Scanner(System.in);
        return 82.29 * input.nextInt();
    }
}
```
## 7. To calculate Fibonacci Series up to n numbers.
```java
// Type 1
//=======================
public class Main(){
    public static void main(Strings[] args)
    {
        Scanner scan = new Scanner(System.in);
        System.out.println("Please enter the nth number");
        int n = scan.next();
        int a = 0,b = 1,c = 1;
        int count = 2;
        if(n == a){
            System.out.println(n+"th is "+a);
        } else if(n == b){
            System.out.println(n+"th is "+b);
        }else {
            while(count<=n){
            c = b + a;
            a = b;
            b = c;
            count++;
            }
            System.out.println(n+"th is "+c);
        }
    }
}
//Type 2
//========================
import java.util.Scanner;

public class fibo {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Please enter number ");
        fibonacci(input.nextInt());
    }
    static void fibonacci(int num) {
        int a = 0, b=1,c = 1;
        System.out.print(a+", ");
        while (c<num){
            System.out.print(c+", ");
            c = a+ b;
            a = b;
            b = c;

        }
        

    }
}

```
## 8. To find out whether the given String is Palindrome or not.
```java
//This program runs on NUMBERS
import java.util.Scanner;

public class palindrome {
    public static void main(String[] args) {
        Scanner input  = new Scanner(System.in);
        System.out.println(palind(input.nextInt()));
    }
    static boolean palind(int number){
        int orig = number;
        int reverse = 0;
        while(number > 0){
            int temp = number % 10;
            reverse = reverse * 10 + temp;
            number/=10;
        }
        return orig == reverse;
    }
}
```
## 9. To find Armstrong Number between two given 3 digit numbers.
```java
import java.util.Scanner;

public class Armstrong {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        String ans = find(input.nextInt() , input.nextInt());
        System.out.println(ans);
    }
    static String find(int num1, int num2){
        int orig1 = num1;
        int sum1 = 0;
        while(num1 > 0) {
            int temp = num1 % 10;
            sum1 = temp * temp * temp + sum1;
            num1 /= 10;
        }
        int orig2 = num2;
        int sum2 = 0;
        while(num2 > 0) {
            int temp = num2 % 10;
            sum2 = temp * temp * temp + sum2;
            num2 /= 10;
        }
        if (sum1 == orig1 && sum2 == orig2){
            return "Both are Armstrong";
        } else if (sum1 == orig1 && sum2 != orig2){
            return sum1 + " 1st number is Armstrong";
        } else if (sum1 != orig1 && sum2 == orig2){
            return sum2 + " 2nd numerb is Armstrong";
        } else {
            System.out.println(sum1 +" "+ sum2);
            return "Both are not Armstrong";
        }
    }

}
```

xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
IIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIII
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
IIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIIII
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx


# 03 Conditionals Loops
## Basic Java Programs
### 1. Area Of Circle Java Program
```java
import java.util.Scanner;

public class Area {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Please Enter the Radius: ");
        System.out.print(circle(input.nextInt()));
    }
    static double circle(int radius){
		// πr<sup>2</sup> = area of circle
        double PI = 3.14;
        return PI*radius*radius;
    }
}
```
### 2. Area Of Isosceles Triangle

```java
import java.util.Scanner;
public class Area {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println(triangle(input.nextInt(),input.nextInt()));
    }
    static double triangle(int base,int height){
             return (base*height)/2;
    }
}

```
### 3. Area of Rectangle
```java
import java.util.Scanner;

public class Area {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println(rectanle(input.nextInt(),input.nextInt()));
    }
 
    static double rectangle(int height,int width){
        return height * width;
    }
}
```

### 4. Area Of Parallelogram
```java
import java.util.Scanner;

public class Area {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println(parallelogram(input.nextInt(),input.nextInt()));
    }
 
    static double parallelogram(int height,int base){
        return height * base;
    }
}
```

### 5. Area Of Rhombus
```java
import java.util.Scanner;

public class Area {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println(rhombus(input.nextInt(),input.nextInt()));
    }
 
    static double rhombus(int diagonal1,int diagonal2){
        return (diagonal1 * diagonal2)/2;
    }
}
```

### 6. Area Of Equilateral Triangle
```java
import java.util.Scanner;

public class Area {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println(equiTriangle(input.nextInt()));
    }
 
    static double equiTriangle(int side){
        return Math.sqrt(3)/4*side*side;
    }
}
```


### 7. Perimeter Of Circle
```java
import java.util.Scanner;

public class Area {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println(periCircle(input.nextInt()));
    }
  static double periCircle(int radius){
		// 2πr = perimeter of circle
        double PI = 3.14;
        return 2*PI*radius;
    }
}
```

### 8. Perimeter Of Equilateral Triangle
```java
import java.util.Scanner;

public class Area {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println(periEquiTriangle(input.nextInt()));
    }
  static double periEquiTriangle(int side){
		// P=3a = perimeter of Equilateral Triangle
        return 3*side;
    }
}
```
### 9. Perimeter Of Parallelogram
```java
import java.util.Scanner;

public class Area {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println(periParallelogram(input.nextInt(),input.nextInt()));
    }
  static double periParallelogram(int side1,int side2){
		// P=2(a+b) = Perimeter Of Parallelogram
        return 2*(sied1 +side2);
    }
}
```

### 10. Perimeter Of Rectangle
```java
import java.util.Scanner;

public class Area {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println(periRectangle(input.nextInt(),input.nextInt()));
    }
  static double periRectangle(int length,int width){
		// P=2(l+w) = Perimeter Of Rectangle
        return 2*(length + width);
    }
}
```
### 11. Perimeter Of Square
```java
import java.util.Scanner;

public class Area {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println(periSquare(input.nextInt()));
    }
  static double periSquare(int side){
		// P = 4a Perimeter Of Square
        return 4*side;
    }
}
```

### 12. Perimeter Of Rhombus
```java
import java.util.Scanner;

public class Area {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println(periRhombus(input.nextInt()));
    }
  static double periRhombus(int side){
		// P = 4a Perimeter Of Rhombus
        return 4*side;
    }
}
```

### 13. Volume Of Cone
```java
import java.util.Scanner;

public class Area {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println(volumeCone(input.nextInt(),input.nextInt()));
    }
  static double volumeCone(int rad, int height){
		// V=πr<sup>2</sup>(h/3) Volume Of Cone
		double PI = 3.14;
        return PI*rad*rad*(height/3);
    }
}
```

### 14. Volume Of Prism
```java
import java.util.Scanner;

public class Area {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println(volumePrism(input.nextInt(),input.nextInt()));
    }
  static double volumePrism(int rad, int height){
		// V=Area of Base * height
		// v = BH ===> (1/2 bh)H
		// b = side1
		// h = side2
		// H = Height
		double PI = 3.14;
        return PI*rad*rad*(height/3);
    }
}
```
### 15. Volume Of Cylinder
```java
import java.util.Scanner;

public class Area {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println(volumeCylinder(input.nextInt(),input.nextInt()));
    }
  static double volumeCylinder(int rad, int height){
		// V=πr<sup>2</sup>h
		double PI = 3.14;
        return PI*rad*rad*height;
    }
}
```

### 16. Volume Of Sphere
```java
import java.util.Scanner;

public class Area {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println(volumeSphere(input.nextInt()));
    }
  static double volumeSphere(int rad){
		// V=(4/3)πr<sup>3</sup>
		double PI = 3.14;
        return (4/3)*PI*rad*rad*rad;
    }
}
```

### 17. Volume Of Pyramid
```java
import java.util.Scanner;

public class Area {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println(volumeSphere(input.nextInt(),input.nextInt(),input.nextInt()));
    }
  static double volumeSphere(int length,int width, int height){
		// V=lwh/3
        return (length*width*height)/3;
    }
}
```

### 18. Curved Surface Area Of Cylinder
```java
import java.util.Scanner;

public class Area {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println(surfaceCylinder(input.nextInt(),input.nextInt()));
    }
  static double surfaceCylinder(int rad, int height){
		// V=2πrh
		double PI = 3.14;
        return 2*PI*rad*height;
    }
}
```

### 19. Total Surface Area Of Cube
```java
import java.util.Scanner;

public class Area {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println(surfaceCube(input.nextInt()));
    }
  static double surfaceCube(int rad, int height){
		// V=6a<sup>2</sup>
		double PI = 3.14;
        return 6*rad*rad;
    }
}
```

### 20. Fibonacci Series In Java
```java
import java.util.Scanner;

public class Fibonacci {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        fibo(input.nextInt());
    }
  static void fibo(int n){
		int firstTerm = 0, secondTerm = 1;
		for (int i = 1; i <= n; ++i) {
			System.out.print(firstTerm + ", ");

		    // compute the next term
		    int nextTerm = firstTerm + secondTerm;
		    firstTerm = secondTerm;
		    secondTerm = nextTerm;
		}
    }
}
```

### 21. Given an integer number n, return the difference between the product of its digits and the sum of its digits.
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print(sumOfDigits(input.nextInt()));
    }
  static int sumOfDigits(int n){
        int product = 1, sum = 0;
        while(n>0){
            int temp = n%10;
            product*=temp;
            sum+=temp;
            n/=10;
        }
        return product - sum;
    }
}
```

### 22. Input a number and print all the factors of that number (use loops).
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        factors(input.nextInt());
    }
   static void factors(int n){
        for (int i = 2; i < n; i++) {
            if(n % i ==0){
                System.out.print(i+" ");
            }
        }
    }
}
```

### 23. Take integer inputs till the user enters 0 and print the sum of all numbers (HINT: while loop)
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        sumOfNumbers();
    }
   static void sumOfNumbers(){
        Scanner input = new Scanner(System.in);
        int sum = 0;
        while(true){
            System.out.println("Please Enter number or Zero to exit");
            int ans = input.nextInt();
            if(ans == 0) break;
            sum = sum + ans;
        }
        System.out.println(sum);
    }
}
```

### 24. Take integer inputs till the user enters 0 and print the largest number from all.
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        largestNumber();
    }
    static void largestNumber(){
        Scanner input = new Scanner(System.in);
        int large = Integer.MIN_VALUE;
        while(true){
            System.out.println("Please Enter number or Zero to exit");
            int ans = input.nextInt();
            if(ans == 0) break;
            if(ans > large){
               large = ans;
            }
        }
        System.out.println(large);
    }
}
```

## Intermediate Java Programs

### 1. Factorial Program In Java
