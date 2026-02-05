# Day 06 – Selection Sort

## What is Selection Sort?
Selection Sort is a sorting algorithm that repeatedly selects the smallest element from the unsorted part and places it at the beginning.

## How it Works
- Find the minimum element in the array
- Swap it with the first element
- Move to the next position
- Repeat until the array is sorted

## Time Complexity
- Best Case: O(n²)
- Average Case: O(n²)
- Worst Case: O(n²)

## Advantages
- Simple to understand
- Performs fewer swaps than Bubble Sort

## Disadvantages
- Inefficient for large datasets
- Always takes O(n²) time

## Example (C)
```c
int arr[5] = {64, 25, 12, 22, 11};
for(int i = 0; i < 5; i++) {
    int min = i;
    for(int j = i + 1; j < 5; j++) {
        if(arr[j] < arr[min]) {
            min = j;
        }
    }
    int temp = arr[min];
    arr[min] = arr[i];
    arr[i] = temp;
}
