# Day 04 – Searching (Binary Search)

## What is Binary Search?
Binary Search is an efficient searching algorithm that works on a **sorted array**.
It repeatedly divides the search interval in half.

## Conditions
- Array must be **sorted**
- Works best on large datasets

## Algorithm
1. Set low = 0 and high = n - 1
2. Find mid = (low + high) / 2
3. If arr[mid] == key → element found
4. If key < arr[mid] → search left half
5. If key > arr[mid] → search right half
6. Repeat until low > high

## Example (C)
```c
int binarySearch(int arr[], int n, int key) {
    int low = 0, high = n - 1;
    while (low <= high) {
        int mid = (low + high) / 2;
        if (arr[mid] == key)
            return mid;
        else if (key < arr[mid])
            high = mid - 1;
        else
            low = mid + 1;
    }
    return -1;
}
