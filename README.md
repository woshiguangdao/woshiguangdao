#include <stdio.h>

int l(int n)
{
	if(n==1||n==0)
	return 1;
	else
	{
	int a=1;
	a=n*l(n-1);
	return(a);
    }
}
int z(int n,int r)
{
	int m=l(n)/(l(r)*l(n-r));
	return m;
}
void yang(int n)
{
//	if(n==1)
	//printf("1\n1 1");
	//else
	for(int i=0;i<=n;i++)
	{
		for(int j=0;j<=i;j++)
		{
			printf("%5d",z(i,j));
		}
		printf("\n");
	}
}
int main()
{
	int row;
	printf("请输入正整数:");
	scanf("%d",&row);
	yang(row);
	return 0;
}
