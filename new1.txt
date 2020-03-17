#include<stdio.h>
#include<stdlib.h>
 int main()
{
	int m,n,p,q,i,j,k,a[10][10],b[10][10],c[10][10];
	printf("Enter the order of the matrix A\n");
	scanf("%d%d",&m,&n);
	printf("Enter the order of the matrix B\n");
	scanf("%d%d",&p,&q);
	if(n!=p)
	{
		printf("Matrix multiplicaton cannot be possible");
		exit(0);
	}
	printf("Enter the elements to the matrix A\n");
	for(i=0;i<m;i++)
	{
		for(j=0;j<n;j++)
		{
			scanf("%d",&a[i][j]);
		}
	}
	printf("Enter the elements to the matrix B\n");
	for(i=0;i<p;i++)
	{
		for(j=0;j<q;j++)
		{
			scanf("%d",&b[i][j]);
		}
	}
	for(i=0;i<m;i++)
	{
		for(j=0;j<q;j++)
		{
			c[i][j]=0;
			for(k=0;k<p;k++)
			{
				c[i][j]+=a[i][k]*b[k][j];
			}
		}
	}
	printf("Matrix A\n");
		for(i=0;i<m;i++)
	{
		for(j=0;j<n;j++)
		{
			printf("%d\t",a[i][j]);
		}
		printf("\n");
	}
	printf("Matrix B\n");
		for(i=0;i<p;i++)
{
	
		for(j=0;j<q;j++)
		{
				printf("%d\t",b[i][j]);

		}
		printf("\n");
}

			
	printf("The Resultant Matrix is\n");
		for(i=0;i<m;i++)
		{
			for(j=0;j<q;j++)
			{
				printf("%d\t",c[i][j]);
		
			}
			printf("\n");
	
		}
}

