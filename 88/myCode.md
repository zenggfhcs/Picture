## 我的代码
```
class Solution {
    public void merge(int[] nums1, int m, int[] nums2, int n) {
        int i=0;
        int j=0;
        int k;
        while(j<n&&i<m+n){
            if(nums2[j]<nums1[i]){
                for(k=j+m;k>i;k--){
                    nums1[k]=nums1[k-1];
                }
                nums1[i]=nums2[j];
                j++;
            }else{
                i++;
            }
        }
        while(j<n){
            nums1[m+j]=nums2[j++];
        }
    }
}
```
