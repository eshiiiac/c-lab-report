## 1) length of string w/o using strlen()
```
#include <stdio.h>
int main(){
    char w[100];
    int i , count = 0;
    printf("Enter a sentence: ");
    gets(w);
    
    for(i=0; w[i]!='\0';i++){
        count++;
    }
    printf("count = %d", count);
    return 0;
}
```
## 2) input sentence and count vowels
```
#include <stdio.h>
int main(){
    char w[100];
    int i , count = 0;
    printf("Enter a sentence: ");
    gets(w);
    
    for(i=0; w[i]!='\0';i++){
       if(w[i]=='a'||w[i]=='e'||w[i]=='i'||w[i]=='o'||w[i]=='u'||w[i]=='A'||w[i]=='E'||w[i]=='I'||w[i]=='O'||w[i]=='U'){
           count++;
       }
    }
    printf("count = %d", count);
    return 0;
}
```
## 3 input 3 words and print three shortest word
```
#include <stdio.h>
#include <string.h>
int main(){
    char w[50],x[50],y[50];
    int len_x,len_y,len_w;
    int i , count = 0;
    printf("Enter 3 words: ");
    scanf("%s%s%s",w,x,y);
    
len_w = strlen(w);
len_x = strlen(x);
len_y = strlen(y);

    if(len_w <= len_x && len_w <= len_y) {
        printf("%s is the shortest\n", w);
    } else if(len_x <= len_w && len_x <= len_y) {
        printf("%s is the shortest\n", x);
    } else {
        printf("%s is the shortest\n", y);
    }
    return 0;
}
```
## palindrome word
```
#include <stdio.h>
#include <string.h>
int main(){
    char w[50],x[50];
    printf("Enter word: ");
    scanf("%s",w);
    
strcpy(x,w);

strrev(strlwr(w));

if(strcmp(w,x)==0){
    printf("Plaindrome");
}
else{
    printf("not Palindrome");
}
    return 0;
}
```
## 
```
N
Ne
Nep
Nepa
Nepal
```
```
#include <stdio.h>
#include <string.h>
int main(){
    char w[]="Nepal";
    int i,j,k;
    
    for(i=0;i<=4;i++){
    	for(j=0;j<=i;j++){
    		printf("%c",w[j]);
		}
		printf("\n");
	}

    return 0;
}
```
## Q 5 B
```
  N
 NEP
NEPAL
```
```
#include <stdio.h>
int main(){
    char w[]="Nepal";
    int i,k,j,sp=5;
  
  	for(i=0;i<5;i+=2){
  		for(k=1;k<sp;k++){
  			printf(" ");
		  }
		  for(j=0;j<=i;j++){
		  	printf("%c",w[j]);
		  }
		  printf("\n");
		  sp--;
	  }
  
    return 0;
}

```
