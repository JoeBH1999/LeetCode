# 第88题
~~~java
class Solution {
    public void merge(int[] nums1, int m, int[] nums2, int n) {
        int nums1Index = m-1, nums2Index = n-1, newIndex = m+n-1;
        while(newIndex >= 0){
            nums1[newIndex--] = (nums2Index < 0 || (nums1Index >= 0 && nums1[nums1Index] > nums2[nums2Index])) 
                ? nums1[nums1Index--]  : nums2[nums2Index--] ;
        }
    }
}
~~~