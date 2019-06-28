# matrix-multiplication

#include<stdio.h>
 
int main()
{
    int a[10][10],b[10][10],c[10][10],i,j,k,r1,c1,r2,c2;
 
    printf("Enter number of rows and columns of matrix1: \n");
    scanf("%d%d",&r1,&c1);
    printf("Enter number of rows and columns of matrix2: \n");
    scanf("%d%d",&r2,&c2);
    if(r2==c1)
    {
 
        printf("\n Enter values for Matrix1:");
 
        for(i=0; i<r1; i++)
        {
            for(j=0; j<c1; j++)
                scanf("%d",&a[i][j]);
        }
 
        printf("\n Enter values for Matrix2: ");
        for(i=0; i<r2; i++)
        {
            for(j=0; j<c2; j++)
                scanf("%d",&b[i][j]);
        }
 
        printf("The First Matrix Is: \n");
        
        for(i=0; i<r1; i++)
        {
            for(j=0; j<c1; j++)
                printf(" %d ",a[i][j]);
            printf("\n");
        }
 
        printf("The Second Matrix Is:\n");
        for(i=0; i<r2; i++)
        {
            for(j=0; j<c2; j++)
                printf(" %d ",b[i][j]);
            printf("\n");
        }
 
 
        printf("the result is:\n");
 
        for(i=0; i<r1; i++)
        {
            for(j=0; j<c2; j++)
            {
                c[i][j]=0;
                for(k=0; k<r1; k++)
                    c[i][j]+=a[i][k]*b[k][j];
                printf("%d  ",c[i][j]);
            }
            printf("\n");
        }
 
    }
    else
    {
        printf("Matrix Multiplication is Not Possible");
    }
    return 0;
}
