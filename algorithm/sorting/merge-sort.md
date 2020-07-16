# Merge Sort

**Merge Sort** is a Divide-and-Conquer technique. 

1. **Divide** the array by half. Recursively divide the half arrays until there are no more half arrays to divide. 
2. **Conquer** sort the divided arrays in each step. 
3. **Combine** by merging the two sorted half arrays into one sorted array.

![Merge Sort Process \(source: Runestone Academy\)](../../.gitbook/assets/mergesorta.png)

### Complexity Analysis

Time Complexity: for all cases \(worst, average, and best\): $$O(n\log n)$$

Space Complexity: $$O(n)$$ 

### Example Code:

```text
public class MergeSort {

    private void sort(int[] A) {
        int[] temp = new int[A.length];
        mergeSort(A, 0, A.length - 1, temp);
    }

    private void mergeSort(int[] A, int start, int end, int[] temp) {
        if (start >= end) {
            return;
        }

        int mid = start + (end - start) / 2;

        mergeSort(A, start, mid, temp);
        mergeSort(A, mid + 1, end, temp);
        merge(A, start, mid, end, temp);
    }

    private void merge(int[] A, int start, int mid, int end, int[] temp) {
        int left = start;
        int right = mid + 1;
        int index = start;

        // merge two sorted subarrays in A to temp array
        while (left <= mid && right <= end) {
            if (A[left] < A[right]) {
                temp[index++] = A[left++];
            } else {
                temp[index++] = A[right++];
            }
        }
        while (left <= mid) {
            temp[index++] = A[left++];
        }
        while (right <= end) {
            temp[index++] = A[right++];
        }

        for (index = start; index <= end; index++) {
            A[index] = temp[index];
        }
    }
}

```

