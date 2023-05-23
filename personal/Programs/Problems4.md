## Submit the following on your Leetcode profile itself.
> CLICK on ***solution*** to see the Solutions.
### Easy
1. [Build Array from Permutation](https://leetcode.com/problems/build-array-from-permutation/)  [solution](#build-array)
2. [Concatenation of Array](https://leetcode.com/problems/concatenation-of-array/)  [solution](#concentration-array)
3. [Running Sum of 1d Array](https://leetcode.com/problems/running-sum-of-1d-array/)  [***solution***](#)
4. [Richest Customer Wealth](https://leetcode.com/problems/richest-customer-wealth/)  [***solution***](#)
5. [Shuffle the Array](https://leetcode.com/problems/shuffle-the-array/)  [***solution***](#)
6. [Kids With the Greatest Number of Candies](https://leetcode.com/problems/kids-with-the-greatest-number-of-candies/)  [***solution***](#)
7. [Number of Good Pairs](https://leetcode.com/problems/number-of-good-pairs/)  [***solution***](#)
8. [How Many Numbers Are Smaller Than the Current Number](https://leetcode.com/problems/how-many-numbers-are-smaller-than-the-current-number/)  [***solution***](#)
9. [Create Target Array in the Given Order](https://leetcode.com/problems/create-target-array-in-the-given-order/)  [***solution***](#)
10. [Check if the Sentence Is Pangram](https://leetcode.com/problems/check-if-the-sentence-is-pangram/)  [***solution***](#)
11. [Count Items Matching a Rule](https://leetcode.com/problems/count-items-matching-a-rule/)  [***solution***](#)
12. [Find the Highest Altitude](https://leetcode.com/problems/find-the-highest-altitude/)  [***solution***](#)
13. [Flipping an Image](https://leetcode.com/problems/flipping-an-image/)  [***solution***](#)
14. [Cells with Odd Values in a Matrix](https://leetcode.com/problems/cells-with-odd-values-in-a-matrix/)  [***solution***](#)
15. [Matrix Diagonal Sum](https://leetcode.com/problems/matrix-diagonal-sum/)  [***solution***](#)
16. [Find Numbers with Even Number of Digits](https://leetcode.com/problems/find-numbers-with-even-number-of-digits/)  [***solution***](#)
17. [Transpose Matrix](https://leetcode.com/problems/transpose-matrix/)  [***solution***](#)
18. [Add to Array-Form of Integer](https://leetcode.com/problems/add-to-array-form-of-integer/)  [***solution***](#)
19. [Maximum Population Year](https://leetcode.com/problems/maximum-population-year/)  [***solution***](#)
20. [Determine Whether Matrix Can Be Obtained By Rotation](https://leetcode.com/problems/determine-whether-matrix-can-be-obtained-by-rotation/)  [***solution***](#)
21. [Two Sum](https://leetcode.com/problems/two-sum/)  [***solution***](#)
22. [Find N Unique Integers Sum up to Zero](https://leetcode.com/problems/find-n-unique-integers-sum-up-to-zero/)  [***solution***](#)
23. [Lucky Number In a Matrix](https://leetcode.com/problems/lucky-numbers-in-a-matrix/)  [***solution***](#)
24. [Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)  [***solution***](#)
25. [Reshape the Matrix](https://leetcode.com/problems/reshape-the-matrix/)  [***solution***](#)
26. [Plus One](https://leetcode.com/problems/plus-one/)  [***solution***](#)
27. [Remove Duplicates from Sorted Array](https://leetcode.com/problems/remove-duplicates-from-sorted-array/)  [***solution***](#)
28. [Minimum Cost to Move Chips to The Same Position](https://leetcode.com/problems/minimum-cost-to-move-chips-to-the-same-position/)  [***solution***](#)

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
