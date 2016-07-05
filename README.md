#include<stdio.h>

void part(int arr[20], int fst, int last);

int main()
{
 
	int arr[30],i,n;
 
	printf("Enter total no. of the elements : ");
	scanf("%d",&n);
 
	printf("Enter total %d elements : \n",n);

	 for(i=0; i<n; i++)
    	
		scanf("%d",&arr[i]);
	   
             part(arr,0,n-1);
 	
	printf("After Partition elements are  : \n");
   
 	 for(i=0; i<n; i++)
  
          printf("%d\t",arr[i]);

 return 0;
}
void swap(int* a, int* b)
{

    int t = *a;

    *a = *b;

    *b = t;

}

void part(int arr[20], int fst, int last)
{

 int i,j,pivot,tmp;

   pivot=fst;

   i=fst;

   j=last;

if(fst<last)
{

    while(arr[i]<=arr[pivot] && i<last)

        i++;

    while(arr[j]>arr[pivot])

        j--;
 
     
  while(i<j)

  {    
     swap(&arr[i], &arr[j]);
	 i++;
	 j--;
     while(arr[i]<=arr[pivot] )

        i++;

     while(arr[j]>arr[pivot])

        j--;   

   }
}
    if ( arr[pivot] < arr[j])
		j--; 
	swap(&arr[j], &arr[pivot]);

	return j;
} 
  
  
 



