# September28_2025
The problem that i solved today in leetcode

Given an integer array nums, return the largest perimeter of a triangle with a non-zero area, formed from three of these lengths. If it is impossible to form any triangle of a non-zero area, return 0.

Code:
class Solution {
    public int largestPerimeter(int[] nums) {
        int n=nums.length;
        Arrays.sort(nums);
        for(int i=n-1;i>=2;i--)
        {
            if(nums[i-1]+nums[i-2]>nums[i])
                return nums[i]+nums[i-1]+nums[i-2];
        }
        return 0;
    }
}
