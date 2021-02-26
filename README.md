# 2021-CLanguage
2021 program in class
## First code (找零錢)50元?個  5元?個  1元?個
```C
#include <stdio.h>
int main()
{
	int a;
	scanf("%d",&a);
	
	printf("%d=50*%d+5*%d+1*%d\n",a,a/50,a%50/5,a%50%5/1);
}
```
## Second code (找因數有幾個)a代表幾個因數
```C
#include <stdio.h>
int main()
{
	int n,a=0;
	scanf("%d",&n);
	
	for(int i=1;i<=n;i++){
		if(n%i==0)
			a++;
	}
	printf("%d\n",a);
}
```
## Third code (找10個數有幾個是3的倍數)
```C
#include <stdio.h>
int main()
{
	int a[10],ans=0;
	for(int i=0;i<10;i++){
		scanf("%d",&a[i]);
	}
	for(int i=0;i<10;i++){
		if(a[i]%3==0)
		ans++;
	}
	printf("%d\n",ans);
}
```
## 4 code (分數等級)
```C
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	
	if(n>=90)printf("A\n");
	else if(n<90 && n>=80)printf("B\n");
	else if(n<80 && n>=60)printf("C\n");
	else printf("F\n");
}
```
## 5 code (分數化簡)
```C
#include <stdio.h>
int main()
{	
	int a,b,big=1;
	scanf("%d%d",&a,&b);
	int max=a;
	if( b>max )max=b;
	for(int i=1;i<=max;i++){
		if(a%i==0 && b%i==0)
			if (i>big)
				big=i;
	}
	printf("%d %d\n",a/big,b/big);
}
```
