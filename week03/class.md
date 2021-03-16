##進階題：計算陣列的平方值
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
