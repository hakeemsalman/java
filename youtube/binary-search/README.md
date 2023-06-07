# Binary Search

```output
Binary Search is defined as a searching algorithm used in a sorted array by repeatedly dividing the search interval in half. The idea of binary search is to use the information that the array is sorted and reduce the time complexity to O(log N). 
```

```java
int[] arr {2,4,6,9,11,12,14,20,36,48};
```  

`target = 36`

> Find the middle element
> target > mid ==> search in the right else search in left
> if middle element == target element ==>` ans`

```java
public class BinarySearch {

    public static void main(String[] args) {
        int[] arr = {-18, -12, -4, 0, 2, 3, 4, 15, 16, 18, 22, 45, 89};
        int target = 22;
        int ans = binarySearch(arr, target);
        System.out.println(ans);
    }

    // return the index
    // return -1 if it does not exist
    static int binarySearch(int[] arr, int target) {
        int start = 0;
        int end = arr.length - 1;

        while(start <= end) {
            // find the middle element
//            int mid = (start + end) / 2; // might be possible that (start + end) exceeds the range of int in java
            int mid = start + (end - start) / 2;

            if (target < arr[mid]) {
                end = mid - 1;
            } else if (target > arr[mid]) {
                start = mid + 1;
            } else {
                // ans found
                return mid;
            }
        }
        return -1;
    }
}
```

## Order Agnostic array Binary searhc

It means whethher the array is in Ascending order or Descending order, but you don't know which one it is. But it is a **Sorted Array**

To overcome this, Order Agnostic Binary Search.

```java
public class OrderAgnosticBS {
    public static void main(String[] args) {
//        int[] arr = {-18, -12, -4, 0, 2, 3, 4, 15, 16, 18, 22, 45, 89};
        int[] arr = {99, 80, 75, 22, 11, 10, 5, 2, -3};
        int target = 22;
        int ans = orderAgnosticBS(arr, target);
        System.out.println(ans);
    }

    static int orderAgnosticBS(int[] arr, int target) {
        int start = 0;
        int end = arr.length - 1;

        // find whether the array is sorted in ascending or descending
        boolean isAsc = arr[start] < arr[end];

        while(start <= end) {
            // find the middle element
//            int mid = (start + end) / 2; // might be possible that (start + end) exceeds the range of int in java
            int mid = start + (end - start) / 2;

            if (arr[mid] == target) {
                return mid;
            }

            if (isAsc) {
                if (target < arr[mid]) {
                    end = mid - 1;
                } else {
                    start = mid + 1;
                }
            } else {
                if (target > arr[mid]) {
                    end = mid - 1;
                } else {
                    start = mid + 1;
                }
            }
        }
        return -1;
    }
}

```



## Binary Search Interview Questions - Google, Facebook, Amazon

NOTE: If you get sorted array, try to use Binary search if working

### Ceiling of a Number

If you have given an array, `arr = {2,3,5,9,14,16,18}`,
Ceiling = smallest element in array greater or equal to target

```
examples:-
--------------------
ceiling(arr, target=14) => 14
ceiling(arr, target=15) => 16
ceiling(arr, target=4) => 5
ceiling(arr, target=9) => 9

```




```java
public class BinarySearch {

    public static void main(String[] args) {
        int[] arr = {-18, -12, -4, 0, 2, 3, 4, 15, 16, 18, 22, 45, 89};
        int target = 22;
        int ans = binarySearch(arr, target); 
        System.out.println(ans);
    }

    // return the index
    // return -1 if it does not exist
    static int binarySearch(int[] arr, int target) {  
        int start = 0;
        int end = arr.length - 1;

        while(start <= end) {
            // find the middle element
//            int mid = (start + end) / 2; // might be possible that (start + end) exceeds the range of int in java
            int mid = start + (end - start) / 2;

            if (target < arr[mid]) {
                end = mid - 1;
            } else if (target > arr[mid]) {
                start = mid + 1;
            } else {
                // ans found
                return arr[mid];
            }
        }
        return arr[start];
    }
}

```


### Find the Floor of a Number

If you have given an array, `arr = {2,3,5,9,14,16,18}`,  

floor number = largest element in array less or equal to target

```
examples:-
--------------------
floor(arr, target=14) => 9
floor(arr, target=15) => 14
floor(arr, target=4) => 3
floor(arr, target=9) => 9

```