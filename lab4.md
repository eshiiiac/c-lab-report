# ARRAY

## WAP TO INPUT NUMBERS IN AN ARRAY OF SIZE 'N' AND FIND THE SUM OF ODD & EVEN NUMBERS SEPARATELY
```
#include <stdio.h>

int main(){
    int arr[1000];
    int n,i,osum=0, esum=0;
    
    printf("enter array size: ");
    scanf("%d",&n);
     printf("Enter %d array elements: ",n);
     for(i=0;i<n;i++){
         scanf("%d",&arr[i]);

         if(arr[i]%2==0){
             esum+=arr[i];
         }
         else{
             osum+=arr[i];
         }
     }
     printf("Sum  of even: %d\n",esum);
     printf("Sum  of odd: %d",osum);
}
```

