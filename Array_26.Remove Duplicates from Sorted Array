  /*
   public int removeDuplicates(int[] nums) {
        if (nums.length==0 || nums.length==1)
            return nums.length;
        int i = 0;
        for (int j = 0; j< nums.length; j++){
            if(nums[j] > nums[i])
                nums[i++] = nums[j];
        }
        return i+1;
       // throw new IllegalArgumentException("No Remove Duplicates solution");
    }
    		Your input:[1,1,2]
				Output:[2,1]
				Expected:[1,2]
        
    Find the problem????
    the problem is in nums[i++] = nums[j];
    */
    
    
    class Solution {
    public int removeDuplicates(int[] nums) {
        //if (nums.length==0 || nums.length==1)
            //return nums.length;
        int i = 0;
        for (int j = 0; j< nums.length; j++){
            if(nums[j] != nums[i]){
                ++i;
                nums[i] = nums[j];
            }

        }
        return i+1;
       // throw new IllegalArgumentException("No Remove Duplicates solution");
    }
}


    Runtime:0 ms, faster than 100.00% of Java online submissions.
		Memory Usage:41.1 MB, less than 32.98% of Java online submissions.
