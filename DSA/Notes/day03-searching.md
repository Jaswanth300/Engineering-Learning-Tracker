# Day 03 – Searching (Linear Search)

## What is Searching?
Searching is the process of finding a specific element in a data structure.

## Linear Search
Linear Search checks each element sequentially until the required element is found or the list ends.

## Algorithm
1. Start from the first element
2. Compare each element with the key
3. If found, return index
4. If not found, return -1

## Example (C)
```c
int linearSearch(int arr[], int n, int key) {
    for (int i = 0; i < n; i++) {
        if (arr[i] == key)
            return i;
    }
    return -1;
}
