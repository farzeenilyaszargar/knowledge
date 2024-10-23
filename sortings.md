# Sortings
### Bubble Sort
it is a simple algorithm that compares every two elements in an array and swaps them based on case (increasing/decreasing).  
<ins>time complexity</ins>: O(n<sup>2</sup>)  
<ins>space complexity</ins>: 1

```c
void bubbleSort(int *arr, int n)
{
    for (int i = 0; i<n; i++)
    {
        for (int j=0; j<i; j++)
        {
            if (arr[i]<arr[j])
            {
                int temp = arr[i];
                arr[i] = arr[j];
                arr[j] = temp;
            }           
        }
    }
}
```
_____

### Selection Sort



_____

### Insertion Sort



_____

### Merge Sort



_____

### Quick Sort


_____

### Counting Sort



_____

### Radix Sort




_____

### Heap Sort





_____

### Bucket Sort




_____

### Shell Sort





_____

  
