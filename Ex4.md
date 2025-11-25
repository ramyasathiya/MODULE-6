## Ex.No:4
## Ex.Name: Remove a Node from a Doubly Linked List using STL
## Date:
## Aim:
To write a C++ program to remove a node from a doubly linked list using STL and display the list before and after removal.

## Algorithm:
Start the program.

Create an STL list<int> to store integer elements.

Insert n elements into the list.

Display the list before removing any element.

Read the element to be removed.

Use the remove() function of STL to delete the specified element.

Display the list after removal.

Stop the program.

## Program:
```
#include <list>
#include <iostream>
using namespace std;

int main() {
    list<int> a;
    int data;

    // Insert 5 elements into the list
    for (int i = 0; i < 5; i++) {
        cin >> data;
        a.push_back(data);
    }

    cout << "List before removing elements: ";
    for (auto it = a.begin(); it != a.end(); it++) {
        cout << *it << " ";
    }

    // Read element to be removed
    cin >> data;
    a.remove(data);

    cout << "\nList after removing elements: ";
    for (auto it = a.begin(); it != a.end(); it++) {
        cout << *it << " ";
    }

    return 0;
}
```
## Output:
<img width="865" height="449" alt="image" src="https://github.com/user-attachments/assets/96d4cff2-f42a-4f2f-bd7a-ad1a012ed0c3" />


## Result:
The Program Executed Successfully.
