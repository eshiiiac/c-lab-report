## sum of digits of a number
```
#include <stdio.h>

int main() {
int n,r,sum=0;
printf("Enter a num: ");
scanf("%d",&n);
   while(n>0){
       r=n%10;
       sum=sum+r;
       n=n/10;
   }
   printf("hhelo");
printf("sum of digits is %d",sum);
    return 0;
}
```
## palindrome number
```
#include <stdio.h>

int main() {
int n,r,sum=0;
printf("Enter a num: ");
scanf("%d",&n);
   while(n>0){
       r=n%10;
       sum=sum*10+r;
       n=n/10;
   }
printf("sum of digits is %d",sum);
    return 0;
}
```
