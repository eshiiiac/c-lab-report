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