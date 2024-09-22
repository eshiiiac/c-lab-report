### fibbonacci series
```
#include <stdio.h>

int fibb(int n);

int main(){
	printf("%d ",fibb(5));
}

int fibb(int n){
	if (n==0){
		return 0;
	}
	else if (n==1){
		return 1;
		
	}
	else
	 return fibb(n-2)+fibb(n-1);
}
```
### WAP to find the nth term of fibonacci series using recursive func
```
#include <stdio.h>

int fibb(int n);

int main(){
	int n;
	printf("enter a num: ");
	scanf("%d",&n);
	printf("%d ",fibb(n));
}

int fibb(int n){
	if (n==0){
		return 0;
	}
	else if (n==1){
		return 1;
		
	}
	else
	 return fibb(n-2)+fibb(n-1);
}
```
