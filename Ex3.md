 ## Ex.No:3
 ## Ex.Name: Modify an Element from a Circular Linked List
 ## Date:
 ## Aim:
To write a C++ program to modify (replace) an element from a circular linked list and display the list before and after modification.

 ## Algorithm:
Start the program.

Define a node class with value and next pointer.

Create a function create(int dat) to insert nodes into the circular linked list.

Create a function display() to print all elements of the list.

Create a function replace(int a, int b) to:

Traverse the circular list.

Find the node with value a and replace it with b.

In the main() function:

Read 5 integers and create the circular linked list.

Display the list.

Read the element to be replaced and the new element.

Call replace() and display the modified list.

Stop the program.
 ## Program:
 ```
#include<iostream>
using namespace std;

class node {
public:
    int value;
    node* next;
} *head, *tail, *temp, *newnode;

void create(int dat) {
    newnode = new node();
    newnode->value = dat;
    newnode->next = NULL;
    if (head == NULL) {
        head = newnode;
        tail = newnode;
    } else {
        tail->next = newnode;
        tail = newnode;
        tail->next = head;
    }
}

void display() {
    temp = head;
    while (temp->next != head) {
        cout << "Data = " << temp->value << " ";
        temp = temp->next;
    }
    cout << "Data = " << temp->value << " ";
}

void replace(int a, int b) {
    temp = head;
    while (temp->next != head) {
        if (temp->value == a) {
            temp->value = b;
            break;
        }
        temp = temp->next;
    }
    if (temp->value == a)  // check last node
        temp->value = b;
}

int main() {
    int data;
    for (int i = 0; i < 5; i++) {
        cin >> data;
        create(data);
    }
    display();

    int x, y;
    cin >> x >> y;
    replace(x, y);

    cout << endl;
    display();
    return 0;
}
```
 ## Output:

<img width="885" height="451" alt="481544867-cbe98852-2b10-4b21-a272-d34a15604077" src="https://github.com/user-attachments/assets/044155f3-ce75-48ee-b112-40be18d14dc9" />


 ## Result:
The Program Executed Successfully.
