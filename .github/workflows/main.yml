#include<stdio.h>
#include<stdlib.h>
/*definition of node*/
struct node{
int data;
struct node*next;
};
struct node*head=NULL;
/*function prototype*/
void create();
void insertAH();
void delete();
void traverse();
/*main function*/
int main()
{
int choice;
while(1)
{
printf("\n----singly linked list AH----\n");
printf("1.create\n");
printf("2.insertAH\n");
printf("3.delete\n");
printf("4.traverse\n");
printf("5.exit\n");
printf("enter your choice:");
scanf("%d",&choice);
switch (choice)
{
case 1:create();
break;
case 2:insertAH();
break;
case 3:delete();
break;
case 4:traverse();
break;
case 5:exit(0);
break;
default:printf("invalid choice\n");
}
}
return 0;
}
void create()
{
int n,i,value;
struct node*temp,*newnode;
printf("enter number of nodes:");
scanf("%d",&n);
for(i=0;i<n;i++)
{
newnode=(struct node*)malloc(sizeof(struct node));
printf("enter data:");
scanf("%d",&value);
newnode->data=value;
newnode->next=NULL;
if(head==NULL)
{
head=newnode;
}
else
{
temp=head;
while(temp->next!=NULL)
temp=temp->next;
temp->next=newnode;
}
}
}
void insertAH()
{
int value;
struct node*newnode,*temp;
newnode=(struct node*)malloc(sizeof(struct node));
printf("enter value to insert:");
scanf("%d",&value);
newnode->data=value;
newnode->next=NULL;
if(head==NULL)
{
head=newnode;
}
else
{
temp=head;
while(temp->next!=NULL)
temp=temp->next;
temp->next=newnode;
}
}
/*Delete a node*/
void delete()
{
int value;
struct node*temp,*prev;
if(head==NULL)
{
printf("list is empty\n");
return;
}
printf("enter value to delete:");
scanf("%d",&value);
temp=head;
if(temp->data==value)
{
head=temp->next;
free(temp);
printf("node deleted\n");
return;
}
while(temp!=NULL&&temp->data!=value)
{
prev=temp;
temp=temp->next;
}
if(temp==NULL)
{
printf("value not found\n");
}
else
{
prev->next=temp->next;
free(temp);
printf("node deleted\n");
}
}
/*Traverse the list*/
void traverse(){
struct node*temp;
if(head==NULL){
printf("list is empty\n:");
return;
}
temp=head;
printf("linked list:");
while(temp!=NULL){
printf("%d->",temp->data);
temp=temp->next;
}
printf("NULL\n");
}
