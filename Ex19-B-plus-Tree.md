# Ex 4(D) B+ Tree
## DATE:
## AIM:
To write a C function to traverse the elements in a B+ Tree.

## Algorithm

1.Start the program.

2.Loop through all keys in the current node.

3.If the node is not a leaf, recursively traverse the child before each key.

4.Print the current key.

5.After the loop, if the node is not a leaf, recursively traverse the last child.

6.End the program.  

## Program:
```
/*
Program to traverse the elements in a B+ Tree.
Developed by: Shree Lekha.S
RegisterNumber: 212223110052
*/

void traverse(struct B_TreeNode *p)
{
    int i;
    for(i=0;i<p->n;i++){
        if(p->leaf==0){
            traverse(p->child_ptr[i]);
        }
        printf("%d ",p->data[i]);
    }
    if(p->leaf==0){
        traverse(p->child_ptr[i]);
    }
}

```

## Output:
![image](https://github.com/user-attachments/assets/5d75fd62-5c5a-4a93-8af7-4710208ac0c3)


## Result:
Thus, the function to traverse the elements in a B+ Tree is implemented successfully.
