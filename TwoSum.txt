class Solution {
    public int[] twoSum(int[] nums, int target) {

        int idx[]=new int[2];
        HashMap<Integer, Integer> hm = new HashMap<>();
        for(int i=0;i<nums.length;i++) {
            if(hm.containsKey(target-nums[i])) {
                idx[0] = hm.get(target-nums[i]);
                idx[1]=i;
            }
            else {
                hm.put(nums[i],i);
            }
        }
        return idx;
    }
}