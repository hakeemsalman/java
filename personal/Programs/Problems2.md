## Condtional Programs

-------------

1. [Area Of Circle Java Program](#1-area-of-circle-java-program)
2. [Area Of Triangle](#2-area-of-isosceles-triangle)
3. [Area Of Rectangle Program](#3-area-of-rectangle)
4. [Area Of Isosceles Triangle](#2-area-of-isosceles-triangle)
5. [Area Of Parallelogram](#4-area-of-parallelogram)
6. [Area Of Rhombus](#5-area-of-rhombus)
7. [Area Of Equilateral Triangle](#6-area-of-equilateral-triangle)
8. [Perimeter Of Circle](#7-perimeter-of-circle)
9. [Perimeter Of Equilateral Triangle](#8-perimeter-of-equilateral-triangle)
10. [Perimeter Of Parallelogram](#9-perimeter-of-parallelogram)
11. [Perimeter Of Rectangle](#10-perimeter-of-rectangle)
12. [Perimeter Of Square](#11-perimeter-of-square)
13. [Perimeter Of Rhombus](#12-perimeter-of-rhombus)
14. [Volume Of Cone Java Program](#13-volume-of-cone)
15. [Volume Of Prism](#14-volume-of-prism)
16. [olume Of Cylinder](#15-volume-of-cylinder)
17. [Volume Of Sphere](#16-volume-of-sphere)
18. [Volume Of Pyramid](#17-volume-of-pyramid)
19. [Curved Surface Area Of Cylinder](#18-curved-surface-area-of-cylinder)
20. [Total Surface Area Of Cube](#19-total-surface-area-of-cube)
21. [Fibonacci Series In Java Programs](#20-fibonacci-series-in-java)
22. [Subtract the Product and Sum of Digits of an Integer](#21-given-an-integer-number-n-return-the-difference-between-the-product-of-its-digits-and-the-sum-of-its-digits)[ - Leetcode Problem](https://leetcode.com/problems/subtract-the-product-and-sum-of-digits-of-an-integer/)
23. [Input a number and print all the factors of that number (use loops).](#22-input-a-number-and-print-all-the-factors-of-that-number-use-loops)
24. [Take integer inputs till the user enters 0 and print the sum of all numbers (HINT: while loop)](#23-take-integer-inputs-till-the-user-enters-0-and-print-the-sum-of-all-numbers)
25. [Take integer inputs till the user enters 0 and print the largest number from all](#24-take-integer-inputs-till-the-user-enters-0-and-print-the-largest-number-from-all)

------

# [Intermediate Java Programs](#intermediate-java-programs)
1. [Factorial Program In Java](#1-factorial-program-in-java)
2. Calculate Electricity Bill
3. Calculate Average Of N Numbers
4. Calculate Discount Of Product
5. Calculate Distance Between Two Points 
6. Calculate Commission Percentage
7. Power In Java
8. Calculate Depreciation of Value
9. Calculate Batting Average
10. Calculate CGPA Java Program
11. Compound Interest Java Program
12. Calculate Average Marks
13. Sum Of N Numbers
14. Armstrong Number In Java
15. Find Ncr & Npr
16. Reverse A String In Java
17. Find if a number is palindrome or not 
18. Future Investment Value
19. HCF Of Two Numbers Program
20. LCM Of Two Numbers
21. Java Program Vowel Or Consonant 
22. Perfect Number In Java
23. Check Leap Year Or Not
24. Sum Of A Digits Of Number
25. Kunal is allowed to go out with his friends only on the even days of a given month. Write a program to count the number of days he can go out in the month of August.
26. Write a program to print the sum of negative numbers, sum of positive even numbers and the sum of positive odd numbers from a list of numbers (N) entered by the user. The list terminates when the user enters a zero.

---

### 1 Area Of Circle Java Program
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
### 2 Area Of Isosceles Triangle

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
### 3 Area of Rectangle
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

### 4 Area Of Parallelogram
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

### 5 Area Of Rhombus
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

### 6 Area Of Equilateral Triangle
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


### 7 Perimeter Of Circle
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

### 8 Perimeter Of Equilateral Triangle
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
### 9 Perimeter Of Parallelogram
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

### 10 Perimeter Of Rectangle
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
### 11 Perimeter Of Square
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

### 12 Perimeter Of Rhombus
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

### 13 Volume Of Cone
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

### 14 Volume Of Prism
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
### 15 Volume Of Cylinder
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

### 16 Volume Of Sphere
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

### 17 Volume Of Pyramid
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

### 18 Curved Surface Area Of Cylinder
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

### 19 Total Surface Area Of Cube
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

### 20 Fibonacci Series In Java
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

### 21 Given an integer number n return the difference between the product of its digits and the sum of its digits
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

### 22 Input a number and print all the factors of that number use loops
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

### 23 Take integer inputs till the user enters 0 and print the sum of all numbers
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

### 24 Take integer inputs till the user enters 0 and print the largest number from all.
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
-----
## Intermediate Java Programs

### 1 Factorial Program In Java
