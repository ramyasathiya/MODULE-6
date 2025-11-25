## Ex.No:5
## Ex.Name: Insert 5 Elements into a Singly Linked List using STL
## Date:
## Aim:
To write a C++ program to insert 5 elements into a singly linked list using STL and display the list.

## Algorithm:
Start the program.

Define a Node class with members data and next.

Write a function push() to insert elements at the beginning of the list.

Insert 5 elements into the list by calling push().

Write a function printList() to traverse and display the list.

Call the function to print all elements of the list.

Stop the program.

## Program:
```
#include <bits/stdc++.h>
using namespace std;

class Node {
public:
    int data;
    Node* next;
};

// Function to insert a node at the beginning
void push(Node** head_ref, int new_data) {
    Node* new_node = new Node();
    new_node->data = new_data;
    new_node->next = (*head_ref);
    (*head_ref) = new_node;
}

// Function to print the linked list
void printList(Node* node) {
    while (node != NULL) {
        cout << node->data << " ";
        node = node->next;
    }
}

int main() {
    Node* head = NULL;

    // Insert 5 elements
    push(&head, 50);
    push(&head, 40);
    push(&head, 30);
    push(&head, 20);
    push(&head, 10);

    cout << "The forward list operation: ";
    printList(head);

    return 0;
}
```
## Output:

<img width="881" height="314" alt="image" src="https://github.com/user-attachments/assets/a67e0dbb-04f5-4b8c-b806-529a8726f567" />



## Result:
The Program Executed Successfully.
