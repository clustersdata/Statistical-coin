# Statistical-coin

Statistical coin

Problem Description

假设一堆由1分、2分、5分组成的n个硬币总面值为m分，求一共有多少种可能的组合方式（某种面值的硬币可以数量可以为0）。

Input

输入数据第一行有一个正整数T，表示有T组测试数据；

接下来的T行，每行有两个数n,m，n和m的含义同上。

Output

对于每组测试数据，请输出可能的组合方式数；

每组输出占一行。

Sample Input

2 3 5 4 8

Sample Output

1 2


代码：

#include <stdio.h>

void main()

{

    int n,m,i,j,k,num,T;
    
    scanf("%d",&T);
    
    while(T--)
    
    {
    
        scanf("%d%d",&n,&m);
        
        num=0;
        
        for(i=0;i<=n;++i)
        
        {
        
            for(j=0;j<=n;j++)
            
            {
            
                for(k=0;k<=n;k++)
                
                {
                
                    if(i+j*2+k*5==m&&i+j+k==n)
                    
                    {num++;}
                    
                }
                
            }
            
        }
        
        printf("%d\n",num);
        
    }
    
}
