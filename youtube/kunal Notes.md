Self Notes taken from Kunal Youtube Videos
# Java

### Static and Dynamic Programming

Static

- Perform type checking at compile time
- Errors will show at compile time
- Need to declare datatype of variables

example: Java

```java
int a = 10; //no error

b = 20; //error

int name = "Salman"; //error
```

Dynamic

- Perform type checking at runtime
- No need to declare a datatype of variables
- Error might not show till program is run

example:Python

```python
a = 10; //no error

a = "Salman"; //no error

```

## Flow Chart

Start / Stop ---> Eclipse shape  
Input / Output ---> Parallergram [Hey take input some Numbers and (output) print their sum]  
Processing ---> Rectangle [adding thier numbers]  
Condition ---> Rhombus shape(Diamond Shape)  
Flow direction of program ---> Array symbol(----------->)

### Prime Number Checker

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

    // Driver Program
    public static void main(String args[])
    {
        if (isPrime(11))
            System.out.println(" true");
        else
            System.out.println(" false");
        if (isPrime(15))
            System.out.println(" true");
        else
            System.out.println(" false");
    }


    // another method to Prime Number

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

## Java Architecture

points need to be added from Kunal.

## Input/Output

Primitive basically that any datatype you cannot break even further.

```java
int money = 234_000_000;

```

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

### Calculator Program

```java
// do it your self
```

## Completed switch case and nested

## Functions and methods

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

## Shadowing

```java
public class Main(){
    int x = 90; // this will be shadowed at line 8
    public static void main(Strings[] args)
    {
       System.out.println(x); // here x = 90
       int x = 40;
       System.out.println(x); // here x = 40
       fun();
    }
    static void fun(){
        System.out.println(x);
    }
}
```

## ArmStrong Numer

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

## Arrays and ArrayList

### Array 
```java
import java.util.Arrays;
import java.util.Scanner;

public class Input {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        // array of primitives
        int[] arr = new int[5];
        arr[0] = 23;
        arr[1] = 45;
        arr[2] = 233;
        arr[3] = 543;
        arr[4] = 3;
        // [23, 45, 233, 543, 3]
        System.out.println(arr[3]);

        // input using for loops
        for (int i = 0; i < arr.length; i++) {
            arr[i] = in.nextInt();
        }
//
//        System.out.println(Arrays.toString(arr));

//        for (int i = 0; i < arr.length; i++) {
//            System.out.print(arr[i] + " ");
//        }

//        for(int num : arr) { // for every element in array, print the element
//            System.out.print(num + " "); //  here num represents element of the array
//        }

//        System.out.println(arr[5]); // index out of bound error

        // array of objects
        String[] str = new String[4];
        for (int i = 0; i < str.length; i++) {
            str[i] = in.next();
        }

        System.out.println(Arrays.toString(str));

        // modify
        str[1] = "kunal";

        System.out.println(Arrays.toString(str));
    }
}
```
```java
public class Main {

    public static void main(String[] args) {
        // Q: store a roll number
        int a = 19;

        // Q: store a person's name
        String name = "Kunal Kushwaha";

        // Q: store 5 roll numbers
        int rno1 = 23;
        int rno2 = 55;
        int rno3 = 18;

        // syntax
        // datatype[] variable_name = new datatype[size];
        // store 5 roll numbers:
//        int[] rnos = new int[5];
//        // or directly
//        int[] rnos2 = {23, 12, 45, 32, 15};

        int[] ros; // declaration of array. ros is getting defined in the stack
        ros = new int[5]; // initialisation: actually here object is being created in the memory (heap)

//        System.out.println(ros[1]);

        String[] arr = new String[4];
        System.out.println(arr[0]);

//        for (String element : arr) {
//            System.out.println(element);
//        }

    }
}
```
### 2D Array
```java
import java.util.Arrays;
import java.util.Scanner;

public class MultiDimension {
    public static void main(String[] args) {
        /*
             1 2 3
             4 5 6
             7 8 9
        */
        Scanner in = new Scanner(System.in);
//        int[][] arr = new int[3][];

//        int[][] arr = {
//                {1, 2, 3}, // 0th index
//                {4, 5}, // 1st index
//                {6, 7, 8, 9} // 2nd index -> arr[2] = {6, 7, 8, 9}
//        };

        int[][] arr = new int[3][3];
        System.out.println(arr.length); // no of rows
        // input

        for (int row = 0; row < arr.length; row++) {
            // for each col in every row
            for (int col = 0; col < arr[row].length; col++) {
                arr[row][col] = in.nextInt();
            }
        }

        // output
//        for (int row = 0; row < arr.length; row++) {
//            // for each col in every row
//            for (int col = 0; col < arr[row].length; col++) {
//                System.out.print(arr[row][col] + " ");
//            }
//            System.out.println();
//        }

        // output
//        for (int row = 0; row < arr.length; row++) {
//            System.out.println(Arrays.toString(arr[row]));
//        }

        for(int[] a : arr) {
            System.out.println(Arrays.toString(a));
        }
    }
}
```

```java
public class ColNoFixed {
    public static void main(String[] args) {
        int[][] arr = {
                {1, 2, 3, 4},
                {5, 6},
                {7, 8, 9}
        };

        for (int row = 0; row < arr.length; row++) {
            for (int col = 0; col < arr[row].length; col++) {
                System.out.print(arr[row][col] + " ");
            }
            System.out.println();
        }
    }
}
```
### ArrayList
```java
import java.util.ArrayList;
import java.util.Scanner;

public class ArrayListExample {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        // Syntax
        ArrayList<Integer> list = new ArrayList<>(5);

//        list.add(67);
//        list.add(234);
//        list.add(654);
//        list.add(43);
//        list.add(654);
//        list.add(8765);

//        System.out.println(list.contains(765432));
//        System.out.println(list);
//        list.set(0, 99);
//
//        list.remove(2);
//
//        System.out.println(list);

        // input
        for (int i = 0; i < 5; i++) {
            list.add(in.nextInt());
        }

        // get item at any index
        for (int i = 0; i < 5; i++) {
            System.out.println(list.get(i)); // pass index here, list[index] syntax will not work here
        }

        System.out.println(list);



    }
}
```
```java
import java.util.ArrayList;
import java.util.Scanner;

public class MultiAL {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        ArrayList<ArrayList<Integer>> list = new ArrayList<>();

        // initialisation
        for (int i = 0; i < 3; i++) {
            list.add(new ArrayList<>());
        }

        // add elements
        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++) {
                list.get(i).add(in.nextInt());
            }
        }

        System.out.println(list);
    }
}
```
# DSA
## Linear Search Algorithm
> Start searching from First point and find each index to match your requirement until the end.
> arr = [19,12,9,14,77,50] ; size = 6
> find whether 14 exits in array or not
> if no value find, return -1
```output
Time complexity:
best: `O(1)`
worst case: `O(N)`
```
```java
public class Main {

    public static void main(String[] args) {
	    int[] nums = {23, 45, 1, 2, 8, 19, -3, 16, -11, 28};
	    int target = 19;
	    boolean ans = linearSearch3(nums, target);
        System.out.println(ans);
    }

    // search the target and return true or false
    static boolean linearSearch3(int[] arr, int target) {
        if (arr.length == 0) {
            return false;
        }

        // run a for loop
        for (int element : arr) {
            if (element == target) {
                return true;
            }
        }
        // this line will execute if none of the return statements above have executed
        // hence the target not found
        return false;
    }

    // search the target and return the element
    static int linearSearch2(int[] arr, int target) {
        if (arr.length == 0) {
            return -1;
        }

        // run a for loop
        for (int element : arr) {
            if (element == target) {
                return element;
            }
        }
        // this line will execute if none of the return statements above have executed
        // hence the target not found
        return Integer.MAX_VALUE;
    }

    // search in the array: return the index if item found
    // otherwise if item not found return -1
    static int linearSearch(int[] arr, int target) {
        if (arr.length == 0) {
            return -1;
        }

        // run a for loop
        for (int index = 0; index < arr.length; index++) {
            // check for element at every index if it is = target
            int element = arr[index];
            if (element == target) {
                return index;
            }
        }
        // this line will execute if none of the return statements above have executed
        // hence the target not found
        return -1;
    }

}
   
 ```
 Search in Srings
 ```java
 import java.util.Arrays;

public class SearchInStrings {
    public static void main(String[] args) {
        String name = "Kunal";
        char target = 'u';
//        System.out.println(search(name, target));

        System.out.println(Arrays.toString(name.toCharArray()));
    }


    static boolean search2(String str, char target) {
        if (str.length() == 0) {
            return false;
        }

        for(char ch : str.toCharArray()) {
            if (ch == target) {
                return true;
            }
        }
        return false;
    }

    static boolean search(String str, char target) {
        if (str.length() == 0) {
            return false;
        }

        for (int i = 0; i < str.length(); i++) {
            if (target == str.charAt(i)) {
                return true;
            }
        }
        return false;
    }
}
 ```
