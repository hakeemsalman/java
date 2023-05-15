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
