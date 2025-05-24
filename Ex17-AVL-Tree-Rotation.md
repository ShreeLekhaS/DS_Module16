# Ex 4(B) AVL Tree – Rotation
## DATE:
## AIM:
To write a C function to perform right rotation in an AVL Tree.

## Algorithm

1.Start the program and Identify the node x where imbalance occurs due to insertion in the left subtree.

2.Set y as the left child of x.

3.Move y's right subtree to x's left.

4.Make x the right child of y.

5.Update the height of node x.

6.Update the height of node y and return y as the new root of the rotated subtree.

## Program:
```
/*
Program to perform right rotation in AVL Tree
Developed by: Shree Lekha.S
RegisterNumber:212223110052 
*/

/*
typedef struct node
{
int data;
struct node *left,*right;
int ht;
}node;
node *insert(node *,int);
//node *Delete(node *,int);
void preorder(node *);
//void inorder(node *);
int height( node *);
node *rotateright(node *);
node *rotateleft(node *);
node *RR(node *);
node *LL(node *);
node *LR(node *);
node *RL(node *);
*/
node * rotateright(node *x)
{
    node *y=x->left;
    x->left=y->right;
    y->right=x;
    x->ht=height(x);
    y->ht=height(y);
    return y;
}

```

## Output:

![image](https://github.com/user-attachments/assets/961ee124-2c35-4b56-91b0-1c3a73c3e423)




## Result:
Thus, the function to perform right rotation in an AVL Tree is implemented successfully.
