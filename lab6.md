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
### WAP to print first 10 terms of fibonacci series using recursive func
```
#include <stdio.h>

int fibb(int n);

int main(){
	int i,n;
	for(i=1;i<=10;i++){
	printf("%d ",fibb(i));	
	}
	
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

### multiply 2 nums uding recursive func
```
#include <stdio.h>

int multiply(int a, int b);

int main(){
	int a,b;
	printf("nter 2 num: ");
	scanf("%d%d",&a,&b);
printf("%d ",multiply(a,b));
}

int multiply(int a , int b){
	if (b==1){
		return a;
	}
	else
	return a+multiply(a,b-1);
}
```
