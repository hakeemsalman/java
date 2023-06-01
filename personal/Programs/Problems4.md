## Submit the following on your Leetcode profile itself.
> CLICK on ***solution*** to see the Solutions.
### Easy
1. [Build Array from Permutation](https://leetcode.com/problems/build-array-from-permutation/)  &rarr;[solution](#build-array)&larr;
2. [Concatenation of Array](https://leetcode.com/problems/concatenation-of-array/)  &rarr;[solution](#concentration-array)&larr;
3. [Running Sum of 1d Array](https://leetcode.com/problems/running-sum-of-1d-array/) &rarr;[solution](#running-sum)&larr;
4. [Richest Customer Wealth](https://leetcode.com/problems/richest-customer-wealth/)  &rarr;[solution](#richest-customer-wealth)&larr;
5. [Shuffle the Array](https://leetcode.com/problems/shuffle-the-array/)   &rarr;[solution](#shuffle-the-array)&larr;
6. [Kids With the Greatest Number of Candies](https://leetcode.com/problems/kids-with-the-greatest-number-of-candies/)   &rarr;[solution](#kids-candies)&larr;
7. [Number of Good Pairs](https://leetcode.com/problems/number-of-good-pairs/)   &rarr;[solution](#number-of-good-pairs)&larr;
8. [How Many Numbers Are Smaller Than the Current Number](https://leetcode.com/problems/how-many-numbers-are-smaller-than-the-current-number/)   &rarr;[solution](#smaller-than-current-number)&larr;
9. [Create Target Array in the Given Order](https://leetcode.com/problems/create-target-array-in-the-given-order/)   &rarr;[solution](#)
10. [Check if the Sentence Is Pangram](https://leetcode.com/problems/check-if-the-sentence-is-pangram/)   &rarr;[solution](#check-sentence-pangram)&larr;
11. [Count Items Matching a Rule](https://leetcode.com/problems/count-items-matching-a-rule/)   &rarr;[solution](#)
12. [Find the Highest Altitude](https://leetcode.com/problems/find-the-highest-altitude/)   &rarr;[solution](#)
13. [Flipping an Image](https://leetcode.com/problems/flipping-an-image/)   &rarr;[solution](#)
14. [Cells with Odd Values in a Matrix](https://leetcode.com/problems/cells-with-odd-values-in-a-matrix/)   &rarr;[solution](#)
15. [Matrix Diagonal Sum](https://leetcode.com/problems/matrix-diagonal-sum/)   &rarr;[solution](#)
16. [Find Numbers with Even Number of Digits](https://leetcode.com/problems/find-numbers-with-even-number-of-digits/)  [***solution***](#)
17. [Transpose Matrix](https://leetcode.com/problems/transpose-matrix/)   &rarr;[solution](#)
18. [Add to Array-Form of Integer](https://leetcode.com/problems/add-to-array-form-of-integer/)   &rarr;[solution](#)
19. [Maximum Population Year](https://leetcode.com/problems/maximum-population-year/)   &rarr;[solution](#)
20. [Determine Whether Matrix Can Be Obtained By Rotation](https://leetcode.com/problems/determine-whether-matrix-can-be-obtained-by-rotation/)  &rarr;[solution](#)
21. [Two Sum](https://leetcode.com/problems/two-sum/)   &rarr;[solution](#)
22. [Find N Unique Integers Sum up to Zero](https://leetcode.com/problems/find-n-unique-integers-sum-up-to-zero/)   &rarr;[solution](#)
23. [Lucky Number In a Matrix](https://leetcode.com/problems/lucky-numbers-in-a-matrix/)   &rarr;[solution](#)
24. [Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)   &rarr;[solution](#)
25. [Reshape the Matrix](https://leetcode.com/problems/reshape-the-matrix/)   &rarr;[solution](#)
26. [Plus One](https://leetcode.com/problems/plus-one/)   &rarr;[solution](#)
27. [Remove Duplicates from Sorted Array](https://leetcode.com/problems/remove-duplicates-from-sorted-array/)   &rarr;[solution](#)
28. [Minimum Cost to Move Chips to The Same Position](https://leetcode.com/problems/minimum-cost-to-move-chips-to-the-same-position/)   &rarr;[solution](#)

### Medium
1. [Spiral Matrix](https://leetcode.com/problems/spiral-matrix/)  [***solution***](#)
2. [Spiral Matrix II](https://leetcode.com/problems/spiral-matrix-ii/)  [***solution***](#)
3. [Spiral Matrix III](https://leetcode.com/problems/spiral-matrix-iii/)  [***solution***](#)
4. [Set Matrix Zeroes](https://leetcode.com/problems/set-matrix-zeroes/)  [***solution***](#)
5. [Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)  [***solution***](#)
6. [Find First and Last Position of Element in Sorted Array](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/)   [***solution***](#)
7. [Jump Game](https://leetcode.com/problems/jump-game/)  [***solution***](#)
8. [Rotate Array](https://leetcode.com/problems/rotate-array/)  [***solution***](#)
9. [Sort Colors](https://leetcode.com/problems/sort-colors/)  [***solution***](#)
10. [House Robber](https://leetcode.com/problems/house-robber/)  [***solution***](#)

### Hard
1. [Max Value of Equation](https://leetcode.com/problems/max-value-of-equation/)  [***solution***](#)
2. [First Missing Positive](https://leetcode.com/problems/first-missing-positive/)  [***solution***](#)
3. [Good Array](https://leetcode.com/problems/check-if-it-is-a-good-array/)  [***solution***](#)

# Solutions

## Build Array
```java
class Solution {
    public int[] buildArray(int[] nums) {
        int[] ans = new int[nums.length];
        for(int i = 0;i< nums.length;i++){
            ans[i] = nums[nums[i]];
        }
        return ans;
    }
}
```
## Concentration Array
```java
// My solution
class Solution {
    public int[] getConcatenation(int[] nums) {
        int[] ans = new int[2 * nums.length];
      
        for(int i = 0;i< nums.length;i++) {
            ans[i] = nums[i];
        }
        for (int j = 0; j <  nums.length; j++) {
            ans[nums.length +j] = nums[j];
        }
        return ans;
    }
}

// Somebody answer in discussion by Bhaskar-Kumar

class Solution {
    public int[] getConcatenation(int[] nums) {
        int[] res= new int[2*nums.length];

        for(int i=0; i<res.length;i++){
            if(i<nums.length){
                res[i]=nums[i];
            }else{
                res[i]=nums[i-nums.length];
            }
        }

        return res;
    }
}    
```

## Running Sum
```java
class Solution {
    public int[] runningSum(int[] nums) {
         int[] sum = new int[nums.length];
         int temp = 0;
        for (int i = 0; i < nums.length; i++) {
              temp += nums[i];
              sum[i]=temp;
        }
        return sum;
    }
}
```
## Richest Customer Wealth

```java
class Solution {
    public int maximumWealth(int[][] accounts) {
        int sum = 0,max = Integer.MIN_VALUE;
        for (int i = 0; i < accounts.length; i++) {
            for (int j = 0; j < accounts[i].length; j++) {
                sum+=accounts[i][j];
            }
            if(sum > max ){
                max = sum;
            }
            sum = 0;
        }
        return max;
    }
}
```

## Shuffle the Array

```java
// 43.2 MB
class Solution {
    public int[] shuffle(int[] nums, int n) {
        int[] res = new int[nums.length];
        int count = 0;
        for(int i = 0 ; i < nums.length;i++){
            if(i%2==0){
                res[i]=nums[count++];
            } else res[i]=nums[n++];
        }
        return res;
    }
}


// This below have 44MB space complexity
class Solution {
    public int[] shuffle(int[] nums, int n) {
        int[] res = new int[nums.length];
        int count = 0;
        for(int i = 0 ; i < nums.length;i++){
            if(i%2==0){
                res[i]=nums[count++];
            } else res[i]=nums[n++];
        }
        return res;
    }
}
```
## Kids Candies
```java
import java.util.ArrayList;
class Solution {
    public List<Boolean> kidsWithCandies(int[] candies, int extraCandies) {
        ArrayList<Boolean> great = new ArrayList<>();
        int max = 0;
        for(int i = 0;i<candies.length;i++ ){
            if(candies[i] > max){
                max = candies[i];
            }
        }
        for(int j = 0;j<candies.length;j++){
            if(candies[j]+extraCandies >= max) 
                great.add(true);
            else great.add(false);
        }
        return great;
    }
}
```

## Number of Good Pairs
```java
class Solution {
    public int numIdenticalPairs(int[] nums) {
        int count = 0;
        for(int i = 0;i<nums.length;i++){
            for(int j = 0 ;j<i;j++){
                if(nums[i]==nums[j]){
                    count++;
                }
            }
        }
        return count;
    }
}
```

## Smaller than Current Number

> My code in simple terms 14ms 61.44% runtime, 44mb

```java
class Solution {
    public int[] smallerNumbersThanCurrent(int[] nums) {
        int count = 0;
        int[] res = new int[nums.length];
        for (int i = 0; i < nums.length; i++) {
            for (int j = 0; j < nums.length; j++) {
                if (nums[i]>nums[j]) count++;
            }
            res[i] = count;
            count = 0;
        }
        return res;
    }
}
```
> Code by equ1n0x 1ms 100% runtims, 43.8 mb
```java
int[] count = new int[101];
        int[] res = new int[nums.length];
        
        for (int i =0; i < nums.length; i++) {
            count[nums[i]]++;
        }
        
        for (int i = 1 ; i <= 100; i++) {
            count[i] += count[i-1];    
        }
        
        for (int i = 0; i < nums.length; i++) {
            if (nums[i] == 0)
                res[i] = 0;
            else 
                res[i] = count[nums[i] - 1];
        }
        
        return res;      
```

## Check Sentence Pangram

```java
                    //  My program own program O(n2)
public class Main{

    public static void main(Strings[] args){
        System.out.println(checkIfPangram("thequickbrownfoxjumpsoverthelazydog"));
    }
    public boolean checkIfPangram(String sentence) {
       int count = 0;
        for(int i = 97;i<=122;i++) {
            for (int j = 0; j < sentence.length(); j++) {
                if (sentence.charAt(j) == (char) i) {
                    count++;
                    break;
                }
            }
        }
        return count == 26;
    }

}

                    // Leetcode Solution
public class Main{
    public static void main(Strings[] args){
        System.out.println(checkIfPangram("thequickbrownfoxjumpsoverthelazydog"));
    }
    public boolean checkIfPangram(String sentence) {
        for (int i = 0; i < 26; ++i) {
            char currChar = (char)('a' + i);
            if (sentence.indexOf(currChar) == -1)
                return false;
        }
        return true;
    }
}


```



