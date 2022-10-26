# Merge Sort
## [16,21,11,8,12,22]
- ### Write the stages of the given array according to the sort type
    - The Merge Sort algorithm is a sorting algorithm that is based on the Divide and Conquer paradigm. In this algorithm, the array is initially divided into two equal halves and then they are combined in a sorted manner.

|Steps|Dividing and Merging|
|:--:|:--:|
|Divide #1|[16,21,11] - [8,12,22]|
|Divide #2|[16,21] - [11] - [8,12] - [22]|
|Divide #3|[16] - [21] - [11] - [8] - [12] - [22]|
|Merge #1|[16,21] - [11] - [8,12] - [22]|
|Merge #2|[11,16,21] - [8,12,22]|
|Merge #3|[8,11,12,16,21,22]|
- ### Write the Big-O Notation
    - Merge Sort is a recursive algorithm and time complexity can be expressed as following recurrence relation.
        - T(n) = 2T(n/2) + O(n)
        - The solution of the above recurrence is O(nLogn)

## Pseudocode

```
//Dividing the Array

mergesort(array a)
    if(n == 1)
        return a

    arrayOne = a[0] ... a[n/2]
    arrayTwo = a[n/2+1] ... a[n]

    arrayOne = mergesort (arrayOne)
    arrayTwo = mergesort (arrayTwo)

    return merge(arrayOne, arrayTwo)    
```

```
//Merging the Array

merge(array a, array b)
    array c

    while(a and b have elements)
        if(a[0] > b[0])
            add b[0] to the end of c
            remove b[0] from b
        else
            add a[0] to the end of c
            remove a[0] from a

    //At this point, either a or b is empty

    while(a has elements)
        add a[0] to the end of c
        remove a[0] from a

    while(b has elements)
        add b[0] to the end of c
        remove b[0] from b

    return c
```