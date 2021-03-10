#### 31. Partition Array
Given an array nums of integers and an int k, partition the array (i.e move the elements in "nums") such that:

All elements < k are moved to the left
All elements >= k are moved to the right
Return the partitioning index, i.e the first index i nums[i] >= k.

##### 样例
Example 1:

Input:
[],9
Output:
0

Example 2:

Input:
[3,2,2,1],2
Output:1
Explanation:
the real array is[1,2,2,3].So return 1
##### 挑战
Can you partition the array in-place and in O(n)?

#####注意事项
- You should do really partition in array nums instead of just counting the numbers of integers smaller than k.
- If all elements in nums are smaller than k, then return nums.length

1.Solution1 - Not Recommend
Time Complexity: O(nlogn)
- Sort the array
- Binary Search
```java
public class Solution {
    /**
     * @param nums: The integer array you should partition
     * @param k: An integer
     * @return: The index after partition
     */
    public int partitionArray(int[] nums, int k) {
        // write your code here
        if(nums.length == 0 || nums == null) return 0;

        int start = 0, end = nums.length -1;
        Arrays.sort(nums);

        if(nums[end] < k) return nums.length;

        while(start + 1 < end){
            int mid = (start+end)/2;
            if(nums[mid] == k){
                while(mid > 0 && nums[mid] == nums[mid -1]){
                    -- mid;
                }
                return mid;
            }
            else if(nums[mid] > k){
                end = mid;
            }
            else {
                start = mid;
            }
        }

        if(nums[end] < k) return end;
        return start;
        
    }
}
```

2. Solution2 - QuickSort
Time Complexity: O(n)
TestCase:[3,2,1], k = 2;
[3,2,3,3,2,1], k = 2;
```java
public class Solution {
    /**
     * @param nums: The integer array you should partition
     * @param k: An integer
     * @return: The index after partition
     */
    public int partitionArray(int[] nums, int k) {
        // write your code here
        if(nums == null || nums.length == 0) return 0;
        int left = 0, right = nums.length -1;
        //QuickSort
        while(left <= right){
            while(left <= right && nums[left] < k){
                ++ left;
            }
            while(left <= right && nums[right] >= k){
                -- right;
            }

            if(left <= right){
                int temp = nums[left];
                nums[left] = nums[right];
                nums[right] = temp;
                -- right;
                ++ left;
            }
        }

        return left;
    }
}
```
