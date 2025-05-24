# Ex20 AVL Tree - Deletion
## DATE:
## AIM:
To write a C function to delete an element from an AVL Tree.
## Algorithm

1.Start the program and check if the tree is empty; if yes, return NULL.

2.If the value to delete is greater than current node's data, recursively delete from the right subtree and rebalance if needed.

3.If the value is less, recursively delete from the left subtree and rebalance if needed.

4.If the value matches the current node, and the node has a right child, find the inorder successor (smallest in right subtree), replace current node’s data with successor’s data, then delete successor recursively and rebalance.

5.If no right child exists, replace the node with its left child.

6.Update the node’s height and return the node pointer

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: Shree Lekha.S
RegisterNumber: 212223110052
*/

node * Delete(node *T,int x)
{
    if(T==NULL){
        return NULL;
    }
    else if(x>T->data){
        T->right=Delete(T->right,x);
        if(BF(T)==2){
            if(BF(T->left)>=0){
                T=LL(T);
            }
            else{
                T=LR(T);
                
            }
        }
    }
    else if(x<T->data){
        T->left=Delete(T->left,x);
        if(BF(T)==-22){
            if(BF(T->right)>=0){
                T=RR(T);
            }
            else{
                T=RL(T);
                
            }
        }
    }
    else{
        if(T->right!=NULL){
            node *p;
            p=T->right;
            while(p->left!=NULL){
                p=p->left;
            }
            T->data=p->data;
        T->right=Delete(T->right,p->data);
        if(BF(T)==2){
            if(BF(T->left)>=0){
                T=LL(T);
            }
            else{
                T=LR(T);
            }
        }
        }
        else{
            return T->left;
        }
    }
    T->ht=height(T);
    return T;
}


```

## Output:

![image](https://github.com/user-attachments/assets/f261c6ae-eedf-4204-aa25-d42b15a37f85)


## Result:
Thus, the C program to delete an element from an AVL Tree is implemented successfully.
