//basic_c_code
//Some_basic_programs
#include <stdio.h>
void callbyvalue(int a,int b)
{
    int c=a;
    a=b;
    b=c;
    printf("after swapping value of x=%d and y =%din callbyvalue\n",a,b);
}
void callbyreference(int *a,int *b)
{
    int c=*a;
    *a=*b;
    *b=c;
    printf("value of a=%d and b=%d in callbyreference\n",*a,*b);
}
int main()
{
    int x=10,y=20;
    printf("value of x=%d and y=%d is in main function\n",x,y);
    callbyvalue(x,y);
    printf("value of x=%d and y=%d after call by value function\n",x,y);
    callbyreference(&x,&y);
    printf("value of x=%d and y=%d after call by refernce function\n",x,y);
    return 0;
}
