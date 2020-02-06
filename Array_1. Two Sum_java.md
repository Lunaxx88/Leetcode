/*
Notion:
1.throw new IllegalArgumentException("No two sum solution")
IllegalArgumentException： 非法参数异常

2.twoSum is the name of array, so when we use the value in the array, 
nums [i]

3.return new int[] {i,j};
why we use new?
to create a new object to achieve the data?

4.
What's the difference between int[] twoSum and int[] nums.

5. length of array:
nums.length
*/

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