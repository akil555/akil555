1. Write a program to perform a linear search using recursion.
Answer
// You are using GCC
#include<stdio.h>
int main(){
 int n,i,k,f=1;
 scanf("%d",&n);
 int a[n];
 for(i=0;i<n;i++)
 scanf("%d",&a[i]);
scanf("%d",&k);
 for(i=0;i<n;i++){
 if(k==a[i])
 { printf("Element %d is present at index %d",k,i);
 f=3;
 break;
 }
 else
 f=10;
 }
if(f==10)
  printf("Element %d is not present",k);
}
2. Write a program to perform a linear search using non-recursion.
Answer
// You are using GCC
#include<stdio.h>
int main(){
 int n,i,k,f=1;
 scanf("%d",&n);
 int a[n];
 for(i=0;i<n;i++)
 scanf("%d",&a[i]);
scanf("%d",&k);
 for(i=0;i<n;i++){
 if(k==a[i])
 { printf("Element %d is present at index %d",k,i);
 f=3;
 break;
 }
2. Write a c program to implement shell sort.
Answer
// You are using GCC
#include<stdio.h>
int main(){
 int n,i,temp,j;
 scanf("%d",&n);
 int a[n];
 for(i=0;i<n;i++)
 scanf("%d",&a[i]);
 for(i=0;i<n;i++){
 for(j=i+1;j<n;j++){
 if(a[i]>a[j])
 {temp=a[i];
 a[i]=a[j];
 a[j]=temp;}
 }
 }
 for(i=0;i<n;i++)
 printf("%d ",a[i]);
}
Write a C program that sorts elements of an integer array using Bucket 
sort.
#include <stdio.h>
 
/* Function for bucket sort */
void Bucket_Sort(int array[], int n)
{  
    int i, j;  
    int count[n]; 
    for (i = 0; i < n; i++)
        count[i] = 0;
 
    for (i = 0; i < n; i++)
        (count[array[i]])++;
 
    for (i = 0, j = 0; i < n; i++)  
        for(; count[i] > 0; (count[i])--)
            array[j++] = i;
}   
/* End of Bucket_Sort() */

int main()
{
    int array[100], i, num; 
 
  //  printf("Enter the size of array : ");   
    scanf("%d", &num);   
  //  printf("Enter the %d elements to be sorted:\n",num); 
    for (i = 0; i < num; i++)
        scanf("%d", &array[i]); 
   // printf("\nThe array of elements before sorting : \n");
    for (i = 0; i < num; i++)
        printf("%d ", array[i]);
    printf("\n");
   // printf("\nThe array of elements after sorting : \n"); 
    Bucket_Sort(array, num); 
    for (i = 0; i < num; i++)
        printf("%d ", array[i]);   
    printf("\n");     
    return 0;
}

 f=10;
 }
if(f==10)
printf("Element %d is not present in array",k);
1. Write a program to perform a binary search using recursion.

// You are using GCC
//u5d2
//1
// You are using GCC
#include<stdio.h>
int search(int a[],int i,int n,int k){
 int mid = i+(n-i)/2;
 if(a[mid]==k)
 return mid;
 else if(n<i)
 return -1;
 else if(a[mid]>k)
 return search(a,i,mid-1,k);
 else if(a[mid]<k)
 return search(a,mid+1,n,k);
}
int main(){
 int n;
 scanf("%d",&n);
 int a[n];
 for(int i=0;i<n;i++)
 scanf("%d",&a[i]);
 
 int n2;
 scanf("%d",&n2);
 int pos = search(a,0,n-1,n2);
 if(pos != -1)
 printf("Element %d is present at index %d",n2,pos);
 else
 printf("Element %d is not present in array",n2);
}
2. Write a program to perform a binary search using non-recursion.
// You are using GCC
//u5d2
//1
// You are using GCC
#include<stdio.h>
int search(int a[],int i,int n,int k){
 int mid = i+(n-i)/2;
 if(a[mid]==k)
 return mid;
 else if(n<i)
 return -1;
 else if(a[mid]>k)
 return search(a,i,mid-1,k);
else if(a[mid]<k)
 return search(a,mid+1,n,k);
}
int main(){
 int n;
 scanf("%d",&n);
 int a[n];
 for(int i=0;i<n;i++)
 scanf("%d",&a[i]);
 
 int n2;
 scanf("%d",&n2);
 int pos = search(a,0,n-1,n2);
 if(pos != -1)
 printf("Element %d is present at index %d",n2,pos);
 else
 printf("Element %d is not present in array",n2);
}

//singly linked list with array

//inesrt beg
int main(){
    int n;
    scanf("%d",&n);
    int a[n];
    for(int i=0;i<n;i++)
        scanf("%d",&a[i]);
    int k;
    scanf("%d",&k);
    printf("%d ",k);
    for(int i=0;i<n;i++)
        printf("%d ",a[i]);
} 

//insert_end
int main(){
    int n;
    scanf("%d",&n);
    int a[n];
    for(int i=0;i<n;i++)
        scanf("%d",&a[i]);
    int k;
    scanf("%d",&k);
    for(int i=0;i<n;i++)
        printf("%d ",a[i]);
    printf("%d ",k);
}

//insert_mid 
int main(){
    int n;
    scanf("%d",&n);
    int a[n];
    for(int i=0;i<n;i++)
        scanf("%d",&a[i]);
    int k,pos;
    scanf("%d%d",&pos,&k);
    for(int i=0;i<pos;i++)
        printf("%d ",a[i]);
    printf("%d ",k);
    for(int i=pos;i<n;i++)
        printf("%d ",a[i]);
}

//del_beg
int main(){
    int n;
    scanf("%d",&n);
    int a[n];
    for(int i=0;i<n;i++)
        scanf("%d",&a[i]);
    for(int i=1;i<n;i++)
        printf("%d ",a[i]);
}

//del_end
int main(){
    int n;
    scanf("%d",&n);
    int a[n];
    for(int i=0;i<n;i++)
        scanf("%d",&a[i]);
    for(int i=0;i<n-1;i++)
        printf("%d ",a[i]);
}

//del_mid (index)
int main(){
    int n;
    scanf("%d",&n);
    int a[n];
    for(int i=0;i<n;i++)
        scanf("%d",&a[i]);
    int k;
    scanf("%d",&k);
    for(int i=0;i<n;i++)
        if(i!=k)
            printf("%d ",a[i]);

}

//del_mid (value)
int main(){
    int n;
    scanf("%d",&n);
    int a[n];
    for(int i=0;i<n;i++)
        scanf("%d",&a[i]);
    int k;
    scanf("%d",&k);
    for(int i=0;i<n;i++)
        if(i!=a[k])
            printf("%d ",a[i]);

}
//Searching
#include<stdio.h>
#include<stdlib.h>
int main()
{
    int n,i,s,index;
    scanf("%d",&n);
    int a[n];
    for(i=0;i<n;i++)
        scanf("%d",&a[i]);
   
    scanf("%d",&s);
    for(i=0;i<n;i++)
    {
        if(a[i]==s)
        {
            printf("Element %d is present at index %d",s,i);
            return 0;
        }
    }
    printf("Element %d is not present in array",s);
}
