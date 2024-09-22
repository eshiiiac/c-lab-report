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

# Dynamic memory allocation

- The statement int a[100]; creates 100 memory blocks that occupy 100x2=200 or 100x4=400 bytes of memory.
- However, during progeam execution this all these memory blocks may not be used or also the no. of memory blocks may not be sufficient 
- this creates either wastage or shotage of memory blocks
- to solve this problem, we use the concept of dynamic memory allocation
- dma is a feature in c which allows to create required no of memory blocks at runtime which can be resized dynamically for optimum memory utilization
- c provides 4 functions for dma
	- malloc()
	- calloc()
   	- realloc()
    	- free()
  which are defines under  stdlib.h header file
- malloc() and calloc() are used to allocate memory, malloc takes a single argument, calloc takes 2 arguments
- malloc does not initialize the memory block with 0
- realloc is used to resize memory allocated by callor or malloc
- free is used to remove the dynamically allocated memory.

## fix code
```
#include <stdio.h>
int main{
	int n, i, sum=0;
	printf("enter the value of n: ");
	scanf("%d",&n);
	printf("enter %d numbers: ",n);
	
	int *p = (int *)malloc(n*4);
	
	for(i=0;i<n;i++){
		scanf("%d", p);
		sum+=p;
		p++;
	}
	printf("sum= %d", sum);
	free(p);
return 0;}

```
