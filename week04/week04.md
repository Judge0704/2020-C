## 除惡務盡 
```C
#include <stdio.h>
int main()
{
	char a[100];
	scanf("%s",&a);
	
	int i=0;
	while(a[i]!='\0'){
		if(a[i]!='2'){
			printf("%c",a[i]);
		}
	i++;
	}
	printf("\n");
}
```
## 星星等腰三角形
```C
#include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	
	for(int i=1;i<=n;i++){
		for(int j=0;j<(n-i);j++){
			printf(" ");
		}
		for(int j=0;j<(i*2-1);j++){
			printf("*");
		}
	printf("\n");
	}		
}
```
