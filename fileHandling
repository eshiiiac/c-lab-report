### a data file contains name age favulty os so,e students. wap to input name and find it in record

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

