# Ex 4(C) B-Tree
## DATE: 04.04.2025
## AIM:
To write a C function to delete an element in a B Tree.
## Algorithm

1.Start the program.

2.Check if the current node is NULL; if yes, return (nothing to delete).

3.Call the function to delete the item from the current node.

4.If the item is not found in the node, return without any change.

5.If the current node is the root and becomes empty after deletion, update the root to its first child.

6.End the program.  

## Program:
```
/*
Program to write a C function to delete an element in a B Tree
Developed by: Shree Lekha.S
RegisterNumber: 212223110052
*/

void delete(int item, struct BTreeNode *myNode) {
  int flag;

  if (!myNode) {
    return;
  }

  flag = delValFromNode(item, myNode);

  if (!flag) {
    return;
  }
  if (myNode == root && root->count == 0) {
    root = root->linker[0];
  }


}

```

## Output:

![image](https://github.com/user-attachments/assets/bec27b5b-33b5-42ea-bf64-576d6cf8e03c)


## Result:
Thus, the C function to delete an element in a B Tree is implemented successfully.
