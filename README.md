# daimaku
编写函数 int fac(int x)计算 x!的值。在主函数中输入 n 和 m 的值，通过调用函 数 fac 计算Cnm 的值
#include<stdio.h>
long fac(int x);
int main()
{
 int n,m;
 long retn,retm,C;
 printf("请输入n,m\n");
 scanf("%ld%ld",&n,&m);
 while(n<0||m<0||n<m)
 {
  printf("请输入n,m\n");
  scanf("%ld%ld",&n,&m);
 }
 retn=fac(n);
 retm=fac(m);
 C=retn*1.0/fac(n-m)/retm;
 printf("C=%ld",C);
 return 0;
}
long fac(int x)
{
 if(x==0||x==1)
 return 1;
 if(x>1)
 return(x*fac(x-1));
}
