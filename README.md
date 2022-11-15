#include <stdio.h>
int num = 0;
void f(int flower,int store,int sum) 
{
	if(flower>9 || store>5)  
		return;
	if(flower==9 && store==5)     
	{
		if(sum==1)
		{
			num++;
			return;
		}
		else
		    return;
	}
	f(flower+1,store,sum-1);   
	f(flower,store+1,sum*2);   
}

int main ()
{
	f(0,0,2);  
	printf("%d",num);
	return 0;
}
