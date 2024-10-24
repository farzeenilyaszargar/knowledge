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
this sorting works on the principle of divide and conquer. first we divide and keep dividing the array through recursion and then merge them in a sorted arrangement through the merge() function which creates two arrays of left and right and merges them both to get a sorted array recursively.
  
> time complexity: O(nlogn)   
> space complexity: n

```c
void merge(int arr[], int l, int m, int r)
{

    int n1 = m - l + 1;
    int n2 = r - m;

    int L[n1], M[n2];

    for (int i = 0; i < n1; i++)
        L[i] = arr[l + i];
    for (int j = 0; j < n2; j++)
        M[j] = arr[m + 1 + j];

    int i, j, k;
    i = 0;
    j = 0;
    k = l;

    while (i < n1 && j < n2)
    {
        if (L[i] <= M[j])
        {
            arr[k] = L[i];
            i++;
        }
        else
        {
            arr[k] = M[j];
            j++;
        }
        k++;
    }

    while (i < n1)
    {
        arr[k] = L[i];
        i++;
        k++;
    }

    while (j < n2)
    {
        arr[k] = M[j];
        j++;
        k++;
    }
}

void mergeSort(int arr[], int l, int r)
{
    if (l < r)
    {

        int m = l + (r - l) / 2;

        mergeSort(arr, l, m);
        mergeSort(arr, m + 1, r);

        merge(arr, l, m, r);
    }
}

void printArray(int arr[], int size)
{
    for (int i = 0; i < size; i++)
        printf("%d ", arr[i]);
    printf("\n");
}
```



## Counting Sort




## Radix Sort





## Heap Sort














