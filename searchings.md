# Searchings
no need to understand more because only two matter. but there exist other searching algorithms like interpolation, terinary, exponential etc...

## Linear Search
searching for the target element one by one in a loop  

> Time Complexity: O(n)  
> Space Complexity: O(1)
  
```c
void linearSearch(int *arr, int target, int n)
{
    for (int i = 0; i<n; i++)
    {
        if (arr[i]==target)
        {
            printf("Found at index %d", i);
        }
    }
}
```

## Binary Search
works on sorted arrays by halving the array on each iteration by checking if target element is in the first or the other half.  

> Time Complexity: O(log n)  
> Space Complexity: O(1)


```c
void binarySearch(int *arr, int low, int high, int target)
{
    while (low<=high)
    {
        int mid = low + (high-low)/2;

        if (target==arr[mid])
        {
            printf("Element found at %d", mid);
            break;
        }
        if (target>arr[mid])
        {
            low = mid+1;
        }
        if (target<arr[mid])
        {
            high = mid-1;
        }
    }
}
```
