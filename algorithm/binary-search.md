# Binary Search

#### Classic Problem:

Leetcode 35:[ Search Insert Position](https://leetcode.com/problems/search-insert-position/)

#### Template:

```text
public int searchInsert(int[] nums, int target) {
    if (nums == null || nums.length == 0) return 0;
    
    int start = 0;
    int end = nums.length - 1;
    
    while (start + 1 < end) {
        int mid = start + (end - start) / 2;      
        if (nums[mid] < target) start = mid;
        else if (nums[mid] > target) end = mid;
        else return mid;
    }
    
    if (nums[end] < target) return end + 1;
    else if (nums[start] >= target) return start;
    else return end;
}
```

{% hint style="info" %}
1. _**`while (start + 1 < end)`**_ ensures two pointers will not be the same item.
2. _**`mid = start + (end - start)/2`**_can avoid stackoverflow. 
3. Compare the items of two pointers.
{% endhint %}



#### More Related Problems:

LC278: [First Bad Version](https://leetcode.com/problems/first-bad-version/)





