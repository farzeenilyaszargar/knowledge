# Sortings
most important sortings are quickSort, radixSort, insertionSort & whatever is heap sort important for (idk)


## Bubble Sort
it is a simple algorithm that compares every two elements in an array and swaps them based on case (increasing/decreasing).   
  
> time complexity: O(n<sup>2</sup>)   
> space complexity: 1

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


## Insertion Sort
this sorting works by having two pointers. first we have 'i' which increases every iteration and is the key. then we have 'j' which loops every preceding element and checks if greater or not. if so then all preceding elements are brought forward one step till the condition fails and the last element replaced with key.  
  
> time complexity: O(n<sup>2</sup>)   
> space complexity: 1

```c
void insertionSort(int *arr, int n)
{
    int i, j, key;
    for (i=1; i<n; i++)
    {
        key = arr[i];
        j = i-1;
        while (j>=0 && key<arr[j])
        {
            arr[j+1] = arr[j];
            j--;
        }
        arr[j+1] = key;
    }
}
```

## Selection Sort
this sorting is just swapping the first element selected with minimum element. then the second is swapped with the min of new arr without the first element.
  
> time complexity: O(n<sup>2</sup>)   
> space complexity: 1

```c
void selectionSort(int arr[], int n)
{
    for (int i = 0; i<n-1; i++)
    {
        int min_idx = i;
        for (int j = i+1; i<n; j++)
        {
            if (arr[min_idx]>arr[j])
            {
                min_idx = j;
            }
        }
        int temp = arr[i];
        arr[i] = arr[min_idx];
        arr[min_idx] = temp; 
    }
}

```

## Quick Sort



## Merge Sort






## Counting Sort




## Radix Sort





## Heap Sort















_____

  
