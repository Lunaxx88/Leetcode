## Daily Leetcode - 1.Two Sum

### Information
- Submit Time:
- tag: `Array` `Easy``java`

### Description
Given an array of integers, return indices of the two numbers such that they add up to a specific target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

**Example:**
```
Given nums = [2, 7, 11, 15], target = 9,

Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].

```

### Notion:
```
1.throw new IllegalArgumentException("No two sum solution")
IllegalArgumentException： 非法参数异常

2.twoSum is the name of array, so when we use the value in the array, 
nums [i]

3.return new int[] {i,j};
why we use new?
to create a new object to achieve the data?

4.What's the difference between int[] twoSum and int[] nums.

5. length of array:
nums.length

```
### Solution

```
class Solution {
    public int[] twoSum(int[] nums, int target) {
        for (int i =0; i<nums.length; i++){
            for (int j = 1; j< nums.length; j++){
                if (nums [i] + nums [j] == target){
                    return new int[] {i,j};
                }
            }
        }
            throw new IllegalArgumentException("No two sum solution");
    }
}
```
