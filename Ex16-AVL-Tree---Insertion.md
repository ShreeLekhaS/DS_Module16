# Ex16 AVL Tree - Insertion
## DATE:
## AIM:
To write a C function to insert the elements in an AVL Tree.

## Algorithm

1.Start the program and check if the root is NULL; if so, create a new node.

2.If the value is less than the current node, recursively insert it into the left subtree.

3.If the value is greater than the current node, recursively insert it into the right subtree.

4.After insertion, update the height of the current node.

5.Calculate the balance factor to check if the node is unbalanced.

6.Perform the appropriate rotation (LL, RR, LR, or RL) if the balance factor is ±2.  

## Program:
```
/*
Program to insert the elements in an AVL Tree
Developed by: Shree Lekha.S
RegisterNumber: 212223110052
*/

node * insert(node *T,int x)
{
    if(T==NULL){
        T=(node*)malloc(sizeof(node));
        T->data=x;
        T->left=NULL;
        T->right=NULL;
        T->ht=0;
    }
    else if(x>T->data){
        T->right=insert(T->right,x);
        if(BF(T)==-2){
            if(x>T->right->data){
                T=RR(T);
            }
            else{
                T=RL(T);
            }
        }
    }
    else if(x<T->data){
        T->left=insert(T->left,x);
        if(BF(T)==2){
            if(x>T->left->data){
                T=LL(T);
            }
            else{
                T=LR(T);
            }
        }
    }
    T->ht=height(T);
    return T;
}

```

## Output:

![output](img/avlin.png)

## Result:
Thus, the function to insert the elements in an AVL Tree is implemented successfully in C programming language.
