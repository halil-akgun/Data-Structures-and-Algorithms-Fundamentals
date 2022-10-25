# Insertion Sort
## [22,27,16,2,18,6]
- ### Write the stages of the given array according to the sort type
1. [**22,27**,16,2,18,6]
2. [**16,22,27**,2,18,6]
3. [**2,16,22,27**,18,6]
4. [**2,6,16,22,27**,18]
5. [**2,6,16,18,22,27**]
- ### Write the Big-O Notation
    - The worst-case (and average-case) complexity of the insertion sort algorithm is O(n²). Meaning that, in the worst case, the time taken to sort a list is proportional to the square of the number of elements in the list.
    - The best-case time complexity of insertion sort algorithm is O(n) time complexity. Meaning that the time taken to sort a list is proportional to the number of elements in the list; this is the case when the list is already in the correct order.
- ### After sorting the array, which case does the number 18 belong to?
    - After sorting the array, the number 18 is in the middle of the array, so the number 18 is covered by the average case.
## Pseudocode
```
    for i : 1 to length(A) - 1
        j = i
            while j > 0 and A[j-1] > A[j]
                swap A[j] and A[j-1]
                    j = j - 1
```
- ### Write the first 4 steps of the array [7,3,5,8,2,9,4,15,6] according to Insertion Sort
1. [**3,7**,5,8,2,9,4,15,6]
2. [**3,5,7**,8,2,9,4,15,6]
3. [**3,5,7,8**,2,9,4,15,6]
4. [**2,3,5,7,8**,9,4,15,6]