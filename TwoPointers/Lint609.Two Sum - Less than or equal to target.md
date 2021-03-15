### 609.Two Sum - Less than or equal to target 

**Description**
Given an array of integers, find how many pairs in the array such that their sum is less than or equal to a specific target number. Please return the number of pairs.

**Example**
Given nums = [2, 7, 11, 15], target = 24.
Return 5.
2 + 7 < 24
2 + 11 < 24
2 + 15 < 24
7 + 11 < 24
7 + 15 < 25

#### Solution1: Brute Force

Time Complexity: O(n^2)

No need to remove duplicated values

```
public int twoSum5(int[] nums, int target) {
    //Brute Force
    //O(n^2)
    if(nums.length == 0 || nums == null) return 0;

    int count = 0;
     for(int i = 0; i < nums.length -1; i++){
         int fast = i+1;
      
         while(fast < nums.length && nums[i] + nums[fast] <= target){
             fast++;
             count++;
         }
     }
    return count;
}
```



#### Solution2: Two Pointers

Time Complexity: O(nlogn)

##### Thoughts:

先排序。

左右两个指针，一个往右走，一个往左右。

假设我们发现nums[left] + nums[right] <= target,由于数组排序过，说明在i -j之间的数加起来也是小于target的，不需要重复计算。

```
public int twoSum5(int[] nums, int target) {
    //Brute Force
    //O(n^2)
    if(nums.length == 0 || nums == null) return 0;
    Arrays.sort(nums);
    int left = 0, right = nums.length -1;
    int count = 0;
    while(left < right){
        if(nums[left] + nums[right] <= target){
            count += right - left;
            left ++;
        }
        else{
            right --;
        }
    }
    return count;
}
```