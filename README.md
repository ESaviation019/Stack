#include <stdio.h>

int stk[10];
int top = -1;
void push();
void pop();
void display();

int main()
{
	int ch;
	printf("1. Push 2. Pop 3. Display");
	scanf("%d", &ch);
	switch(ch)
	{
		case 1 : push(); break;
		case 2 : pop(); break;
		case 3 : display();break;
	}
}

void push()
{
	int data;
	if(top == 9)
		printf("overflow");
	else
	{
		scanf("%d", &data);
		top = top + 1;
		stk[top] = data;
	}
}

void pop()
{
	if(top == -1)
	printf("underflow");
	else
		top = top - 1;
}

void display()
{
	int i;
	if(top == -1)
		printf("stack is empty");
	else
		for(i = top; i >= 0; i--);
			printf("%d", stk[i]);
}
