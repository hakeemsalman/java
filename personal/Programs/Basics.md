# Programs

## Level 1

### Difference Between Sum Of Squares
```java
/*
Create a class with a method to find the difference between the sum of the squares and the square of the sum of the first n natural numbers.
Method name: calculateDifference
Argument : int
Return type : int
For eg: if n is 10, you have to find
(1(square)+2(square)+3(square)+.....10(square)) - (1+2+3+.....+10)(square)    

output:
------
Please enter the final number
10
-2640
*/

import java.util.Scanner;
public class Task2 {
	int add,addi,sum,diff;
	public static void main(String[] args) {
		try (Scanner sc = new Scanner(System.in)) {
			int r=sc.nextInt();
			System.out.println(new Task2().calculateDifference(r));
		}
	}
	int calculateDifference(int n) {
		for(int i=1;i<=n;i++) {
			add=i*i;
			addi+=add;//385
		}
		for(int i=1;i<=n;i++) {
			sum+=i;
		}
		sum*=sum;
		diff=addi-sum;
		return diff;
	}
}
```

### Even or Odd
```java
/*
Define a method which returns the 1 if the given number is even, in other case return 0
Name of method: isEven() // which accepts an integer value as argument and return 1 if the given number is even, else retrun 0.
Argument: int
Return type: an integer value 

*/

import java.util.Scanner;

public class Task7 {

	public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		System.out.println("Please enter the number:");
		int x=sc.nextInt();
		System.out.println(new Task7().isEven(x));
	}
	int isEven(int a) {
		if(a%2 ==0) {
			System.out.println("Even");
			a=1;
		}
		else {
			System.out.println("Odd");
			a=0;
		}
		return a;
	}
}
```
### Greatest Number

```java
/*
Define a method which returns the greatest number among two numbers.
Write the method with the following specifications: 
Name of method: getGreatest() // which accepts two integer values as argument and return the greatest value.
Arguments: two argument of type integer
Return type: an integer value 
Specifications: The value returned by the method getGreatest() is determined by the following rules:
If any of the given numbers are negative, return -1.
If any of the given numbers are zero, return -2.
If the given numbers are positive, return the greatest.
*/

import java.util.Scanner;

public class Task8{

	public static void main(String[] args) {
		Scanner scan=new Scanner(System.in);
		System.out.println("Please enter any 2 numbers: ");
		int x=scan.nextInt();
		int y =scan.nextInt();
		System.out.println(new Task8().getGreatest(x,y));
	}
	int getGreatest(int a,int b) {
		int val=0,z=0;
		if(a<0 || b<0) {
			System.out.println("Given numbers are Negative");
			z=-1;
		}
		else if((a!=0 || b!=0) && a>0 || b>0 ) {
			if(a>b) {
				System.out.println("Greatest value: ");
				val=a;
			}
			else {
				System.out.println("Smallest value: ");
				val=b;
			}
			z=val;
		}
		else {
			z=-2;
		}
		return z;
		
	}
}
```

### Least Number
```java
/*
Define a method which returns the least number among two numbers.
Write the method with the following specifications: 
Name of method: getLeastNum() // which accepts two integer values as argument and return the least value.
Arguments: two argument of type integer
Return type: an integer value 
Specifications: The value returned by the method getLeastNum() is determined by the following rules:
If any of the given numbers are negative, return -1.
If any of the given numbers are zero, return -2.
If the given numbers are positive, return the least number.


*/
import java.util.Scanner;

public class Task9 {

	public static void main(String[] args) {
		try (Scanner sc = new Scanner(System.in)) {
			System.out.println("Please enter 2 numbers:");
			int r=sc.nextInt();
			int s=sc.nextInt();
			System.out.println(new Task9().LeastNumber2(r,s));
		}
	}
	int LeastNumber2 (int a,int b) {
		int val=0,z=0;
		if(a<0 || b<0) {
			System.out.println("Given numbers are Negative");
			z=-1;
		}
		else if((a!=0 || b!=0) && a>0 || b>0 ) {
			if(a<b) {
				System.out.println("Greatest value: ");
				val=a;
			}
			else {
				System.out.println("Smallest value: ");
				val=b;
			}
			z=val;
		}
		else {
			z=-2;
		}
		return z;
		
	}

}
```

### Multiplication Table
```java
/*
Display Multiplication number table: 

output:
---------
Please enter the Multiplication number:
5
Please enter the FIRST number: 
1
Please enter the the LAST number:
10
5 x 1 = 5
5 x 2 = 10
5 x 3 = 15
5 x 4 = 20
5 x 5 = 25
5 x 6 = 30
5 x 7 = 35
5 x 8 = 40
5 x 9 = 45
5 x 10 = 50


*/



import java.util.Scanner;

public class MultiplicationTable {
	
	public static void Multiply(int a,int b,int c) {
		for(int i=b;b<=c;b++) {
			System.out.println(a+" x "+b+" = "+a*b);
		}
	}
	public static void main(String[] args) {
		Scanner scan=new Scanner(System.in);
		System.out.println("Please enter the Multiplication number:");
		int multi=scan.nextInt();
		System.out.println("Please enter the FIRST number: ");
		int first=scan.nextInt();
		System.out.println("Please enter the the LAST number:");
		int second =scan.nextInt();
		
		Multiply(multi, first, second);
	}
}
```

### Odd Rounder
```java
/*
Define a method which returns the number it if it is an even number, if the number is odd then return the next multiple of 10.
Write the method with the following specifications: 
Name of method: oddRounder() // which accepts an integer value as argument and return the same value if it is an even number, if the value is odd then return the next multiple of 10. 
Arguments: one argument of type integer
Return Type: an integer value 
+-----------------------------------------------------------------+
+   Example if x = 24 then return 24, if x = 25 then return 30.   +
+-----------------------------------------------------------------+
Specifications: The value returned by the method oddRounder() is determined by the following rules:
If any of the given number is negative, return -1.
If any of the given number is zero, return -2.
If the given number is even, return the same number.
If the given number is odd, return the next multiple of 10.
*/


import java.util.Scanner;

public class Task10 {

	public static void main(String[] args) {
		try (Scanner sc = new Scanner(System.in)) {
			
			int r=sc.nextInt();
			System.out.println(new Task10().oddRounder(r));
		}
	}
	int oddRounder(int a) {
		if(a<0) {
			return-1;
		}
		if(a==0){
			return -2;
		}
		if(a%2!=0) {
			a=a/10;
			a+=1;
			a*=10;
			return a;
		}
		if(a%2==0) {
			return a;
		}
		else {
			return 0;
		}
	}
}
```

### Power of Two
```java
/*
Create a class with a method to check if a number is a power of two or not.
Method name: checkNumber
Argument: int 
Return type: boolean
For eg: 8 is a power of 2 so return true

*/
import java.util.Scanner;

public class Test1 {
	int sum=1;
	public static void main(String[] args) {
		try (Scanner sc = new Scanner(System.in)) {
			int r = sc.nextInt();
			System.out.println(new Test1().checkNumber(r));
		}
	}
	boolean checkNumber(int a) {
		for (int i = 1; i < a ; i++) {
			sum = sum * 2;
			if (sum == a)
				break;
		}
		if (sum == a)
			return true;
		else
			return false;
	}
}

```
### Sum of Digits
```java
/*
Define a method which return the sum of digits of the given two digit number.
Write the method with the following specification:
Name of method getSumOfDigits() // which accepts an integer value as argument and return the sum of it’s digits
Arguments: one argument of type integer
Return type: int
Specification: The value returned by the method getSumOfDigits() is determined by the following rules:
If the given value is in between 10 and 99, return sum of it’s digits.
Example:-
---------
If x = 34, return 7
If the given value is negative, return -3
If the given value is greater than 99, return -2
If the given value is in between 0 and 9, return -1.


*/


import java.util.Scanner;

public class Test1 {
	
	int x,y,sum;
	public static void main(String[] args) {
		try (Scanner sc = new Scanner(System.in)) {
			int x=sc.nextInt();
			System.out.println("Please enter TWO digit number:");
			System.out.println(new Test1().getSumOfDigits(x));
		}
	}
	int getSumOfDigits(int a) {
		if(a>=10 && a<=99) {
			x=a%10;
			y=a/10;
			return x+y;
		}
		if(a<0) {
			return -3;
		}
		if(a>99) {
			return -2;
		}
		if(a>=0 && a<10) {
			return -1;
		}
		else
			return 0;
	}
}
```
### Sum of First N Natural numbers
```java
package prograjfds;

import java.util.Scanner;

public class Test1 {
	/*
	 * Create a class with a method which can calculate the sum of first n natural numbers
	 * which are divisible by 3 or 5
	 * method name:- calculateSum
	 * Argument:- int
	 * Return type:- int
	 */
		int sum;
		public static void main(String[] args) {
			try (Scanner sc = new Scanner(System.in)) {
				int r=sc.nextInt();
				System.out.println(new Test1().calculateSum(r));
			}
		}
		int calculateSum(int n) {
			for(int i=1;i<=n;i++) {
				if(i%3==0 || i%5==0) {
					sum+=i;
				}
			}
			return sum;
		}
	}
```
### Sum of First Three digits
```java
/*
Define a method which returns the sum of three numbers after rounding off each number to the next multiple of 10. If any of the given number is multiple of 10 dont change it's value
Write the method with the following specifications:
Name of method sumofMultiples () // which accepts three integer value as argument and return the sum of three numbers after rounding off each number to the next multiple of 10.
Example
----------
if a = 23, b = 34, c = 69
30+ 40+ 70 = 140 

if a = 23, b = 34, c = 50
30+ 40+ 50 = 120
 
if a = 32 , b = 51, c = 64
40+ 60+ 70 = 170

Arguments: three argument of type integer
Return Type: an integer value Specifications: The value returned by the method sumofMultiples() is determined by the following rules:
if any of the given number is negative or zero, return -1. if the number is an multiple of 10
if the given number is odd, return cube of the given number.


*/

import java.util.Scanner;

public class Task6 {
	int x,y,z,a=1; long q;
	public static void main(String[] args) {
		try (Scanner sc = new Scanner(System.in)) {
			int r=sc.nextInt();
			int s=sc.nextInt();
			int t=sc.nextInt();
			Task6 obj= new Task6();
			System.out.println(obj.sumOfMultiples(r, s, t));
		}
	}
	long sumOfMultiples(int a, int b, int c) {
		if(a<=0 || b<=0 || c<=0) {
			return -1;
		}
		else {
			if(a%10!=0 && a>9) {
				x=a/10;
				x+=1;
				x=x*10;
			}
			else {
				x=a;
			}
			if(b%10!=0 && b>9) {
				y=b/10;
				y+=1;
				y*=10;
				}
			else {
				y=b;
			}
			if(c%10!=0 && c>9) {
				z=c/10;
				z+=1;
				z=z*10;
			}
			else {
				z=c;
			}
			

		}
		if((x+y+z)%2!=0) {
			q=x+y+z;
			q=q*q*q;
			return q;
			}
		else 
			return (x+y+z);
		
	}
}
```

### Three Digit Palindrome
```java
/*
Define a method which returns the 1 if the given three digit number is palindrome, in other case return 0. write the method with the following specifications:
Name of method isPalindrome () // which accepts an integer value as argument and return true if the given number is palindrome, else return false.
Arguments: one argument of type integer
Return Type: an integer value
Specifications: The value returned by the method isPalindrome () is determined
by the following rules:
if the given number is on three digit number, retun 1 if the number is
palindrome, else return 8. Example: if x 232, return 1. if x 345, return
if the given number is negative or zero, return -1
if the given number is not an three digit number, return -2
*/

import java.util.Scanner;

public class Test5 {
	int n,m,y=0,z;
	public static void main(String[] args) {
		try (Scanner sc = new Scanner(System.in)) {
			System.out.println("Please enter THREE digit number:");
			int x=sc.nextInt();
			
			System.out.println(new Test5().isPalindrome(x));
		}
		
	}
	int isPalindrome(int a) 
	{
		
		if(a<=0) {
			return -1;
		}
		if(a>999) {
			return -2;
		}
		if(a>99 && a<1000) {
			m=a;
			while(a!=0) {
				z=a%10;
				y=y*10+z;
				a=a/10;
			}
			if(m==y) {
				System.out.println(y+" is palindrome");
				return 1;
			}
			else {
				System.out.println("Not palindrome");
				return 0;
			}
				
		}
		else 
			return 0;
		
	}
}

```
