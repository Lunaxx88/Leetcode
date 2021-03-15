### 533.Two Sum - Closest to target

**Description**
Given an array nums of n integers, find two integers in nums such that the sum is closest to a given number, target.

Return the difference between the sum of the two integers and the target.



**Example**
Given array nums = [-1, 2, 1, -4], and target = 4.

The minimum difference is 1. (4 - (2 + 1) = 1).



**Challenge**
Do it in O(nlogn) time complexity.



#### Solution1: Two Pointers

Time Complexity: O(nlogn) -- Arrays.sort() function

注意需要取得min的值，每次取最小，因为diff可能会有正负的差别。

```
public int twoSumClosest(int[] nums, int target) {
    if(nums.length == 0 || nums == null) return 0;

    Arrays.sort(nums);
    int left = 0, right = nums.length -1;
    int min = Integer.MAX_VALUE;

    while(left < right){
        int diff = target - nums[left] - nums[right];
        min = Math.min(min, Math.abs(diff));
        if(diff == 0) return 0;
        else if(diff > 0){
            left ++;
        }
        else{
            right --;
        }
    }

    return min;
}
```