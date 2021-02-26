# 2020-C
2020 program in class
## First code (找零錢)
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
