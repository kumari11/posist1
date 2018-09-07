# posist1
#include<iostream>
using namespace std;
struct node
{
int data;
node *nextR;
node *nextL;	
};
class A
{
	node *head;
	node *tail;
	public:
		A()
		{
			head=NULL;
			tail=NULL;
		}
	void insert(int n,int a,int b)
	{
		
		node *temp=new node;
		temp->data=n;
		temp->nextR=NULL;
		temp->nextL=NULL;
		if(head==NULL)
		{
		head=temp;
		tail=temp;
		}
		else
		{
			tail->nextL=temp;
			tail=tail->nextL;
		}
	 	node *temp1=new node;
	 	node *temp2=new node;
	 	temp1->data=a;
	 	temp1->nextL=NULL;
	 	temp1->nextR=NULL;
	 	temp2->data=b;
	 	temp2->nextL=NULL;
	 	temp2->nextR=NULL;
	 	if( temp->nextL==NULL)
{
		if(temp->data>=temp1->data)
	{
		temp->nextL=temp1;
	}
	else
	temp->nextR=temp1;
	 }
}
 
	 void display()
	 {
	 	node *temp1;
	 	temp1=head;
	 	while(temp1->nextL!=NULL)
	 	{
	 		cout<<temp1->data<<endl;
	 		temp1=temp1->nextL;
	 	//	temp1=temp1->nextR;
		 }
	 }

};
int main()
{
	A a;
	a.insert(30,17,10);
	a.display();
	return 0;
}
