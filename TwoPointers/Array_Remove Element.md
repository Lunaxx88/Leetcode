Need to update, this solution is not a good way.

```
class Solution {
    public int removeElement(int[] nums, int val) {
        int n = nums.length;
        if(nums.length == 0 || nums== null) return n;
        
        int i = 0; int j = n-1;
        
        
        while(i<j && n >=0){
            if(nums[j] == val){
                --j;
                --n;
            }
            
            if(i!=j && nums[i] != val){
                i++;
            }
            
            if(i!=j && nums[i] == val && nums[j] != val){
                int tmp;
                tmp = nums[i];
                nums[i] = nums[j];
                nums[j] = tmp;
                
                --j;
                --n;
            }
        }
        
        if(i == j){
            if(nums[i] == val){
                --n;
            }
        }
        
        return n;
    }
}
```
