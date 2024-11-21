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
### create  a menu driven program to add, view, search, delete records, (id name address salary)
```
#include<stdio.h>
#include<string.h>
#include<process.h>

void addRecord(){
	int id, salary;
	char name[20], address[20];

	FILE *ptr = fopen("userData.txt","a");
	
	printf("Enter id, Name, address, salary: ");
	scanf("%d %s %s %d", &id,&name,&address,&salary);
	fprintf(ptr,"%d %s %s %d\n\n", id, name, address, salary);
	fclose(ptr);
}
void viewRecord(){
	int id, salary;
	char name[20], address[20];

	FILE *ptr1 = fopen("userData.txt","r");
	
	
	while(!feof(ptr1)){
		fscanf(ptr1,"%d %s %s %d\n\n", &id,&name,&address,&salary);
		printf("%d %s %s %d\n\n", id, name, address, salary);
	}

	fclose(ptr1);
}
void searchRecord(){
	int id, salary;
	char name[20], address[20], temp_name[20];

	FILE *ptr2 = fopen("userData.txt","r");
	
	
	printf("Search user data, enter id: ");
	scanf("%d",&temp_name);
	
	while(!feof(ptr2)){
		fscanf(ptr2,"%d %s %s %d\n\n", &id,&name,&address,&salary);
		if(strcmpi(name,temp_name)==0){
			printf("%d %s %s %d\n\n", id, name, address, salary);
		}
		else {
			printf("User not found. Error 404\n\n");
		}
	}

	fclose(ptr2);
}
void deleteRecord(){
	int id, salary, temp_id;
	char name[20], address[20];

	FILE *ptr3 = fopen("userData.txt","r");
	FILE *ptr3a = fopen("tempUserData.txt","w");
	
	
	printf("enter id to delete data: ");
	scanf("%d",&temp_id);
	
	while(!feof(ptr3)){
		fscanf(ptr3,"%d %s %s %d\n\n", &id,&name,&address,&salary);
		if(id!=temp_id){
			fprintf(ptr3a,"%d %s %s %d\n", id, name, address, salary);
		}
		else {
			printf("User not found. Error 404\n\n");
		}
	}
	fclose(ptr3);
	fclose(ptr3a);
	remove("userData.txt");
	rename("tempUserData.txt","userData.txt");
	
}

int main(){
	while (1){
	int userChoice;
	printf("1.Add Record\n2.View Record\n3.Search\n4.Delete\nEnter your choice: ");
	scanf("%d",&userChoice);
	
	switch(userChoice){
	
		case 1:
			addRecord();
			break;
		case 2:
			viewRecord();
			break;
		case 3:
			searchRecord();
			break;
		case 4:
			deleteRecord();
			break;
		case 5:
			exit(0);
		default:
			printf("Invalid choice!(enter 1-4)\n\n");
			
		}}
}


```
### wap to store name, faculty age of student and store it in a structure var and store it into a file..(read and write)

```
#include <stdio.h>

struct student
{
	char name[20],faculty[20];
	int age;
}stud;
int main()
{
		FILE *ptr = fopen("studentData.txt","w");
		printf("enter student name, faculty, age: ");
		scanf("%s %d %s",&stud.name,&stud.faculty,&stud.age);
		fwrite(&stud,sizeof(stud),1,ptr);
		fclose(ptr);
		return 0;
}	D
```

### storing in an array of structure
```
#include <stdio.h>

struct student
{
	char name[20],faculty[20];
	int age;
}stud[20];
int main()
{
		int i,n;
		FILE *ptr = fopen("studentData.txt","w");
		
		printf("enter the no. of students: ");
		scanf("%d",&n);
		
		printf("enter student name, faculty, age: ");
		for(i=0;i<n;i++){
		scanf("%s %s %d",&stud[i].name,&stud[i].faculty,&stud[i].age);
		fwrite(&stud[i],sizeof(stud),1,ptr);
		}
		
		fclose(ptr);
		return 0;
		
}
```

### read integers from a file and store odds and evens separately (oddnums.txt, evennums.txt)
```
#include <stdio.h>

int main()
{
		int i,number;
		FILE *ptr = fopen("numbers.txt","r");
		FILE *ptr1 = fopen("evenNumbers.txt","w");
		FILE *ptr2 = fopen("oddNumbers.txt","w");
		
		
		while(!feof(ptr)){
			fscanf(ptr,"%d\n",&number);
			if (number%2==0){
				fprintf(ptr1,"%d\n",number);	
			}
			else{
				fprintf(ptr2,"%d\n",number);
								
			}
		}
		
		fclose(ptr);
		fclose(ptr1);
		fclose(ptr2);
		printf("done");

		return 0;
		
}
```


## notes
### Random Access File
- can be  use  to read & write at any positions ina file
- - fseek(), ftell(), and rewind() methods are used

#### fseek()
syntax
```
int fseek(FILE *PTR, long int position, int origin)
```
- moves \the file pointer(cursor) to the specified position deom the origin
- origin can be 0 (SEEK_SET), 1(SEEK_CUR), 2(SEEK_END)

#### ftell()
```
long int ftell(FILE *ptr)
```
- returns the current position of file pointer

#### rewind()
```
rewinf(FILE *ptr)
```
- moves the file ponter to the beginning of the file
