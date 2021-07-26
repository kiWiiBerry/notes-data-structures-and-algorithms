# Binary Search

#### Classic Problem:

Leetcode 35:[ Search Insert Position](https://leetcode.com/problems/search-insert-position/)

#### Template 0:

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

## Template 1

模板一： 找特定值

```text
int target = value;
int left = 0, right = nums.length - 1;
while (left <= right) {       // !!!  left <= right 
    int mid = left + (right - left) / 2;
    if (nums[mid] == target) {
        return mid;
    } else if (nums[mid] > target) {
        right = mid - 1;      // !!! right = mid - 
    } else {
        left = mid + 1;       // !!! left = mid + 1;
    }
}
```

## Template 2

 模板二：找下界（第一次出现）

```text
int left = 0, right = nums.length - 1;
while (left < right) {
    int mid = left + (right - left) / 2;
    if (nums[mid] >= target) {
        right = mid
    } else {
        left = mid + 1;
    }
}
```

## Template 3

模板三：找上界（最后一次出现）

```text
int left = 0, right = nums.length - 1;
while (left < right) {
    int mid = left + (right - left) / 2 + 1;
    if (nums[mid] <= target) {
        left = mid;
    } else {
        right = mid - 1;
    }
```







