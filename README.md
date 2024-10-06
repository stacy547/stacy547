// C++ program for preorder traversals

#include <bits/stdc++.h>
using namespace std;
struct Node {
    int data;
    struct Node *left, *right;
    Node(int v)
    {
        data = v;
        left = right = nullptr;
    }
};
void printPreorder(struct Node* node)
{
    if (node == nullptr)
        return;
    cout << node->data << " ";
    printPreorder(node->left);
    printPreorder(node->right);
}
int main()
{
    struct Node* root = new Node(1);
    root->left = new Node(2);
    root->right = new Node(3);
    cout << "Preorder traversal of binary tree is: \n";
    printPreorder(root);

    return 0;
}
