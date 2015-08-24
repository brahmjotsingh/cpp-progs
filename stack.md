# cpp-progs
c to cpp data structures.
#include<iostream>
#include<stdio.h>
using namespace std;

class stack{
	private:
		 int top;
		 int arr[10];
		 int max;
		 int data;
		 
	public:
		stack()
		{
			top=0;
			max=5;
		}
		void push()
		{
			if(top==max-1)
			{
					cout<<"stack full";
			}
			else
			{
				cout<<"enter a no";
				cin>>data;
				arr[top++]=data;
			}
		} 
		void pop()
		{
			if(top==0)
				cout<<"\n\nnothing to pop\n";
			else
			{
				
				cout<<"\n\npoped element is "<<arr[--top];
			}
		}
};

int main()
{
	int ch;
	stack ob1;
	
	while(1)
	{
		cout<<"\npress 1 to push\npress 2 to pop\n";
		cin>>ch;
		switch(ch)
		{
			case 1:
				ob1.push();
				break;
			case 2:
				ob1.pop();
				break;
			case 3:
				return 0;
		}
	}
}
