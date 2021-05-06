```
public static void quickSort(int[] arr, int left, int right) {
        if (left > right) {
            return;
        }
        int low = left;
        int high = right;
        int mid = arr[low];
        while (low < high) {
            while (low < high && arr[high] > mid) {
                high--;
            }
            arr[low] = arr[high];
            while (low < high && arr[low] < mid) {
                low++;
            }
            arr[high] = arr[low];
        }
        arr[low] = mid;
        quickSort(arr, left, low - 1);
        quickSort(arr, low + 1, right);
    }
```
