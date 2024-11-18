### a data file contains name age favulty os some students. wap to input name and find it in record

```
#include <stdio.h>
#include <string.h>
int main(){
	
	FILE *ptr= fopen("data.txt", "r");
	char name[20],faculty[20],name1[20];
	int age;
	
	printf("entere name: ");
	scanf("%s",&name1);
	
	while(!feof(ptr)){
	fscanf(ptr,"%s %d %s\n",&name, &age, &faculty);
	}
	if (strcmpi(name,name1)==0){
		printf("%s : name found",name1);
	}
	fclose(ptr);
	
	
}
```
### a data file contains name age favulty os so,e students. wap to input name and delete it from th record

## FIX CODE
```
#include <stdio.h>
#include <string.h>
int main(){
	FILE *ptr1 = fopen("temp.txt", "w");
	FILE *ptr= fopen("data.txt", "r");
	char name[20],faculty[20],name1[20];
	int age;
	
	printf("enter name to delete: ");
	scanf("%s",&name1);
	
	while(!feof(ptr)){
	fscanf(ptr,"%s %d %s\n",&name, &age, &faculty);
}
if (strcmpi(name,name1)!=0){
fprintf(ptr1,"%s %d %s\n",name, age, faculty);
}
	fclose(ptr);
	fclose(ptr1);
	remove("data.txt");
	rename("temp.txt","data.txt");
	
	
}
```
### UPDATING income (salary) of all employess
```
#include <stdio.h>
#include <string.h>
int main(){
	FILE *ptr1 = fopen("temp.txt", "w");
	FILE *ptr= fopen("emp.txt", "r");
	char name[20],address[20];
	int salary;
	
	while(!feof(ptr)){
	fscanf(ptr,"%s %s %d\n",&name, &address, &salary);
	int ns=salary+0.15*salary;
	fprintf(ptr,"%s %s %d\n",name,address, ns)
}
if (strcmpi(name,name1)!=0){
fprintf(ptr1,"%s %d %s\n",name, age, faculty);
}
	fclose(ptr);
	fclose(ptr1);
	remove("emp.txt");
	rename("temp.txt","emp.txt");
	
	
}
```
