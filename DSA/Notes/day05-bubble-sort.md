# Day 05 – Bubble Sort

## What is Bubble Sort?
Bubble Sort is a simple sorting algorithm that repeatedly compares adjacent elements and swaps them if they are in the wrong order.

## How it Works
- Compare adjacent elements
- Swap if the left element is greater
- Repeat for all elements until sorted

## Time Complexity
- Best Case: O(n)
- Average Case: O(n²)
- Worst Case: O(n²)

## Advantages
- Simple to understand
- Easy to implement

## Disadvantages
- Very slow for large datasets
- Not suitable for real-world applications

## Example (C)
```c
int arr[5] = {5, 3, 4, 1, 2};
for(int i = 0; i < 5; i++) {
    for(int j = 0; j < 4 - i; j++) {
        if(arr[j] > arr[j+1]) {
            int temp = arr[j];
            arr[j] = arr[j+1];
            arr[j+1] = temp;
        }
    }
}
