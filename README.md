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
				big=i;
	}
	printf("%d %d\n",a/big,b/big);
}
```
## 6 code(讀入正數反序列印)
```C
#include <stdio.h>
int main()
{
	int a[11],n=0;
	for(int i=0;i<10;i++){
		scanf("%d",&a[i]);
		if(a[i]==0)break;
		n++;
	}
	for(int i=n-1;i>=0;i--){
		printf("%d ",a[i]);
	}
	printf("\n");
}
```
## 7 code(A的B次方函數)
```C
#include <stdio.h>
int MYPOWER(int a,int b)
{	
	int ans;
	for(int i=1;i<b;i++){
		ans*=a;
	}
	return ans;
}
	
	
int main(void)
{
	int a,b;
	scanf("%d%d",&a,&b);
	printf("[%d]",MYPOWER(a,b));
	return 0;
}
```
## 8 code(漸增數列相加)
```C
#include <stdio.h>
int main()
{
	int a;
	scanf("%d",&a);
	int ans=0;
	for(int i=a;i>=0;i--){
		ans+=(i-1)*i;
	}
	printf("%d\n",ans);
}
```

## 9 code(判別正方形)
```C
#include <stdio.h>
int main()
{
	int a,b;
	printf("Enter two numbers:  ");
	scanf("%d%d",&a,&b);
	if(a==b)printf("It is a square ");
	else printf("It is not a square ");
}
	
```
## 10 code(2進位轉10進位)
```C
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	int ans=0;
	ans=(n%10)*1;
	n=n/10;
	ans=(n%10)*2+ans;
	n=n/10;
	ans=(n%10)*4+ans;
	n=n/10;
	ans=(n%10)*8+ans;
	n=n/10;
	printf("%d\n",ans);
}
```

## 11 code (均標與前標計算)
```C
#include <stdio.h>
int main()
{ 
	int sum=0,n,a[100],sumt=0,x=0;
	float avg,avgt;
	scanf("%d",&n);
	
	for(int i=0;i<n;i++){
		scanf("%d",&a[i]);
	}
	for(int i=0;i<n;i++){
		sum+=a[i];
	}
	avg=(float)sum/n;
	printf("均標:%.1f\n",avg);
	
	for(int i=0;i<n;i++){
		if(a[i]>=avg){
		sumt+=a[i];
		x++;
		}
	}
	avgt=(float)sumt/x;
	printf("前標:%.1f\n",avgt);
	
}
```

