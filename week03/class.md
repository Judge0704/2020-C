## 算陣列的平方值
```C
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	int a[10];
	for(int i=0;i<n;i++){
		scanf("%d",&a[i]);
	}
	for(int i=0;i<n;i++){
		printf("%d,",a[i]*a[i]);
	}
	printf("\n");
}
```
## 大小寫轉換
```C
#include <stdio.h>
int main()
{
	char c[10];
	scanf("%s",&c);
	int i=0;
	while(c[i]!='\0'){
		if('A'<=c[i] && c[i]<='Z')
		printf("%c",c[i]-'A'+'a');
		else if('a'<=c[i] && c[i]<='z')
		printf("%c",c[i]-'a'+'A');
		else printf("%c",c[i]);
		i++;
	}
	printf("\n");
}
```
## 計算幾週與幾天
```C
#include <stdio.h>
int main()
{
	int a;
	scanf("%d",&a);
	
	printf("%d %d\n",a/7,a%7);
}
```

## 計程車資計算
```C
#include <stdio.h>
int main()
{
	int a;
	scanf("%d",&a);
	if(a<=2000)printf("100\n");
	else if(a%500==0)printf("%d\n",100+(a-2000)/500*5);
	else printf("%d\n",100+(a-2000)/500*5+5);
}
```
## 兩數間可被5整除的整數	
```C
#include <stdio.h>
int main()
{
	int a,b;
	scanf("%d%d",&a,&b);
	if(a>b){
		for(int i=b;i<=a;i++){
			if(i%5==0)printf("%d\n",i);
		}
	}
	else if(b>a){
		for(int i=a;i<=b;i++){
				if(i%5==0)printf("%d\n",i);
		}	
	}
}
```

## 整數間最大距離
```C
#include <stdio.h>
int main()
{
	int a[3],max,min;
	for(int i=0;i<3;i++){
		scanf("%d",&a[i]);
	}
		min=a[0]; max=a[0];
	for(int i=0;i<3;i++){
		if(min>a[i])min=a[i];
		if(max<a[i])max=a[i];
	}
	printf("%d\n",max-min);
		
}
```
