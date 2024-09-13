# 88. Merge Sorted Array (C Language)

## Problem

Merge nums1 and nums2 into a single array sorted in non-decreasing order.

##### Solution 1.


- Runtime: 6 ms  
- Memory Usage: 9.9 MB

```c
void merge(int* nums1, int nums1Size, int m, int* nums2, int nums2Size, int n) {
    while (m>0 && n>0){
     if(nums2[n-1] >= nums1[m-1]){
        nums1[m+n-1]=nums2[n-1];
        n=n-1;
     }else{
        nums1[m+n-1]=nums1[m-1];
        m=m-1;
     }
    }
    while(n>>0){
        nums1[m+n-1]=nums2[n-1];
        n=n-1;
    }
}
```
