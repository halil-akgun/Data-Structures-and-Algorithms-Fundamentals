# Binary Search Tree

## [7,5,1,8,3,6,0,9,4,2]

- ### Write the Binary-Search-Tree stages of the above array.
    - Binary Search Tree is a node-based binary tree data structure which has the following properties:
        - The left subtree of a node contains only nodes with keys lesser than the node’s key.
        - The right subtree of a node contains only nodes with keys greater than the node’s key.
        - The left and right subtree each must also be a binary search tree.

|     |     |     |     |     |     |     |     |     |     |     |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|     |     |     |     |     |     | 7   |     |     |     |     |
|     |     |     |     |     | /   |     | \   |     |     |     |
|     |     |     |     | 5   |     |     |     | 8   |     |     |
|     |     |     | /   |     | \   |     |     |     | \   |     |
|     |     | 1   |     |     |     | 6   |     |     |     | 9   |
|     | /   |     | \   |     |     |     |     |     |     |     |
| 0   |     |     |     | 3   |     |     |     |     |     |     |
|     |     |     | /   |     | \   |     |     |     |     |     |
|     |     | 2   |     |     |     | 4   |     |     |     |     |

- ### Write the Big-O Notation

    - **Time Complexity**

        - Time complexity of all BST Operations = O(h). Here, h = Height of Binary Search Tree.

    - **Worst Case**

        - In worst case, The binary Search Tree is a skewed binary search tree. Height of the binary search tree becomes n. So, Time complexity of BST Operations = O(n).

    - **Best Case**
        - In best case, The Binary Search Tree is a balanced binary search tree. Height of the binary search tree becomes log(n). So, Time complexity of BST Operations = O(logn).

## Pseudocode

```
//Searching in a Binary Tree

Node search(int x, Node n)
{
    if(n != null)
    {
        if(n.data  == x)
                return (n)
        else if(n.data > x)
                search(x, n.left)
        else
                search(x, n.right)
    }
}
```

```
//Inserting an Element in Binary Tree

insert (Node n, int x)
{
    if (n==null)
    {
        n = new Node(x)
    }
    if(n.data < x)
        insert(n.right, x)
    else if(n.data > x)
        insert(n.left, x)
}
```