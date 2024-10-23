# Sortings
most important sortings are quickSort, radixSort, insertionSort & whatever is heap sort important for (idk)


## Bubble Sort
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

## Insertion Sort
this sorting works by having two pointers. first we have 'i' which increases every iteration and is the key. then we have 'j' which loops every preceding element and checks if greater or not. if so then all preceding elements are brought forward one step till the condition fails and the last element replaced with key.  
  
<ins>time complexity</ins>: O(n<sup>2</sup>)  
<ins>space complexity</ins>: 1

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
_____

## Selection Sort
this sorting
<ins>time complexity</ins>: O(n<sup>2</sup>)  
<ins>space complexity</ins>: 1

```c
dsd
```

_____

## Merge Sort



_____

## Quick Sort


_____

## Counting Sort



_____

## Radix Sort




_____

## Heap Sort





_____

## Bucket Sort




_____

## Shell Sort





_____

  
