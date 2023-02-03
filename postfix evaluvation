#include<stdio.h>
#include<stdlib.h>
#include<ctype.h>
#include<math.h>
#define SIZE 50
int stk[SIZE];
int top=-1;
void push(int elem)
{
  stk[++top]=elem;
  }
int pop()
{
  return stk[top--];
  }
void postfix_eval(char*postfix)
{
  char sym;
  int i=0,op1,op2;
  top=-1;
  while((sym=postfix[i++])!='\0')
    {
      if(isdigit(sym))
        push(sym-'0');
      else
      {
        op2=pop();
        op1=pop();
        switch(sym)
          {
            case '+':push(op1+op2);
            break;
            case '-':push(op1-op2);
            break;
            case '*':push(op1*op2);
            break;
            case '/':push(op1/op2);
            break;
            case '%':push(op1%op2);
            break;
            case '^':push(pow(op1,op2));
            break;
            default :printf("enter the valid expression\n");
            exit(0);
            break;
            }
        }
      }
  printf("the result of the postfix expression is = %d\n",pop());
  }
void main()
{
int ch,n;
char postfix[30];
  while(1)
    {
      printf("1.evaluvation of postfix expression\n");
      printf("2.exit\n");
      printf("enter your choice\n");
      scanf("%d",&ch);
      switch(ch)
        {
          case 1:printf("enter th valid expression with sinle operand only\n");
          scanf("%s",postfix);
          postfix_eval(postfix);
          break;
          case 2:exit(0);
          default :printf("enter the valid choice\n");
          break;
          }
      }
  }
