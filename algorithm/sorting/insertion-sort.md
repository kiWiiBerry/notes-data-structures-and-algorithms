# Insertion Sort

Below is the process demo of insertion sort. It is the simplest way when you are playing poker. 

![Insertion Sort \(Source: brilliant.org\)](../../.gitbook/assets/cgw711m3eo-insertion-set-_1.gif)

### Complexity Analysis

Time Complexity: 

* Worst case: $$O(n^2)$$
* Average case: $$O(n^2)$$ 
* Best case: $$O(n)$$ 

Space Complexity: $$O(1)$$ , since an extra variable `key` is used.

### Example Code:

```text
public class InsertionSort {
    public void sort(int[] arr) {
        int n = arr.length;
        for (int i = 1; i < n; i++) {
            int key = arr[i];
            int j = i - 1;
            
            /* Move the elements of arr[0 to i-1], which are
            greater than key, to one position right
            of their current position */
            while (j >= 0 && arr[j] > key) {
                arr[j + 1] = arr[j];
                j = j - 1;
            }
            arr[j + 1] = key;
        }
    }
}
```

