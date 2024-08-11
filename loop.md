# loop
- a loop is a set of instruction that gets executed repeaedly until the specified condition becomes false
- there are 3 types of ``loop`` in c
    - for loop
    - while oop
    - do while loop

### programs
**expg** _programs_
>P1
```
#include <stdio.h>
int main() {
int i,j;
for(i=1;i<=50;i++){
    if(i%2==0){
          printf("\n%d",i );
    }
}
    return 0;
}
```
>P2

```
#include <stdio.h>
int main() {
int i;
for(i=50;i>=0;i--){
    if(i%2!=0){
          printf("\n%d",i );
    }
}
    return 0;
}
```
>P3

```
#include <stdio.h>
int main() {
int i;
for(i=5;i<=100;i++){
 if(i%5==0){
     printf("\n%d",i);
 }
}
    return 0;
}
```
>P4
```
#include <stdio.h>
int main() {
int i;
for(i=50;i>=1;i--){
 if(i%5==0){
     printf("\n%d",i);
 }
}
    return 0;
}
```
>P5
```
#include <stdio.h>
int main() {
int i;
for(i=1;i<=10;i++){
     printf("\n%d",i*i);
}
    return 0;
}
```
```
#include <stdio.h>
int main() {
int i,n=5,r=5;
for(i=0;i<10;i++){
    printf("\n%d",r=(n*i)+r);
}
    return 0;
}
```

```
#include <stdio.h>
#include <math.h>
// int main() {
// int i,n=5,r=5;
// for(i=0;i<10;i++){
//     printf("\n%d",r=(n*i)+r);
// }
//     return 0;
// }
int main(){
    int i,n=2,r=1;
    for(i=1;i<=20;i++){
        printf("\n%d",r=pow(n,i)+r);
    }
    return 0;
}
```
```
#include <stdio.h>

int main() {
   int i,j;
   for(i=1;i<=5;i++){
       for(j=1;j<=i;j++){
           printf("%d",j);
       }
       printf("\n");
   }

    return 0;
}
```

# output
```
1
12
123
1234
12345
```

```
#include <stdio.h>

int main() {
   int i,j;
   for(i=1;i<=5;i++){
       for(j=1;j<=i;j++){
           printf("%d",i);
       }
       printf("\n");
   }

    return 0;
}
```
#output
```
1
22
333
4444
55555
```

##ascii value
```
#include <stdio.h>

int main() {
   char i,j;
   for(i='a';i<='z';i++){
       for(j='a';j<=i;j++){
           printf("%d ",j);
       }
       printf("\n");
   }


    return 0;
}
```


```
#include <stdio.h>

int main() {
  int i,k,j,sp=5;
  for(i=1;i<=9;i+=2){
      for(k=1;k<=sp;k++){
          printf(" ");
      }
      for(j=1;j<=i;j++){
          printf("%d",j);
      }
      printf("\n");
      sp--;
  }


    return 0;
}

```
#output
```
     1
    123
   12345
  1234567
 123456789

```

## reverse pyramid

```
int main(){
    int i,j,k,sp=0;
    for(i=9;i>0;i-=2){
        for(k=0;k<=sp;k++){
            printf(" ");
        }
        for(j=1;j<=i;j++){
            printf("%d",j);
        }
        printf("\n");
        sp++;
    }
}
```

```
#include <stdio.h>

int main() {
    int i,j,k,sp=5,l;
    for(i=1;i<=5;i++)
    {
        for(k=1;k<=sp;k++)
        {
            printf(" ");
        }
        for(j=i;j>=1;j--)
        {
            printf("%d",j);
        }
        for(l=2;l<=i;l++)
        {
            printf("%d",l);
        }
        printf("\n");
        sp--;
    }
    return 0;
}
```
## output
```
     1
    212
   32123
  4321234
 543212345
```
