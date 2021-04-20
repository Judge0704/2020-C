## UVA10226 Hardwood species
```C
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
int compare(const void *p1, const void *p2)
{
	return strcmp((char*)p1,(char*)p2);
}

char line[1000000][50];
int main()
{
	int T;
	scanf("%d\n\n",&T);
	for(int t=0;t<T;t++){
		int N=0;
		for(int i=0;   ;i++){
			char* now=gets(line[i]);
			if(now==NULL || (strcmp(line[i],"")==0)){
				N=i;
				break;
			}
		}
		qsort(line, N, 50, compare);
		
		if(t>0)printf("\n");
		printf("%s ",line[0]);
		int ans=1;
		for(int i=0;i<N-1;i++){
			if(strcmp(line[i],line[i+1])!=0){
				printf("%.4f\n",100*ans/(float)N);
				printf("%s ",line[i+1]);
				ans=1;
			}else ans++;
		}
		printf("%.4f\n",100*ans/(float)N);
	}
}
```
