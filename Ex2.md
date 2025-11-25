## Ex.No:2
## Ex.Name: Circularly Singly Linked List - Delete an element from the FRONT
## Date:
## Aim:
Write a CPP program to DELETE an element from the FRONT in a Circularly Singly Linked List and Display the same.

## Algorithm:

Start the program.

Create a class Sum that contains overloaded functions:

int add(int a, int b) to return sum of two integers.

int add(int a, int b, int c) to return sum of three integers.

In the main() function:

Read integers from the user.

Call the overloaded functions accordingly.

Display results.

Stop the program.

## Program:
```
#include<iostream>
using namespace std;
class node
{
    public:
    int value;
    node*next;
}*head,*tail,*temp,*newnode;
void deletenode()
{
    head=head->next;
    tail->next=head;
}
void create(int data)
{
    newnode=new node();
    newnode->value=data;
    newnode->next=NULL;
    if(head==NULL)
    {
        head=newnode;
        tail=newnode;
    }
    else
    {
        tail->next=newnode;
        tail=newnode;
        tail->next=head;
    }
}
void display()
{
    temp=head;
    while(temp->next!=head)
    {
        cout<<"Data = "<<temp->value<<" ";
        temp=temp->next;
    }
    cout<<"Data = "<<temp->value<<" ";
}
int main()
{
    int data;
    for(int i=0;i<5;i++)
    {
        cin>>data;
        create(data);
    }
    display();
    deletenode();
    cout<<endl;
    display();
}
```
## Output:

<img width="1174" height="507" alt="image" src="https://github.com/user-attachments/assets/43845ea6-5711-43ed-8019-bb487aca94d1" />


## Result:
The Program Executed Successfully.
