AIM OF THE EXPERIMENT:Program by using Selection sort.

DESCRIPTION OF SELECTION SORT:Selection sort is a simple sorting algorithm.This is an in-place comparison-based algorithm in which the list is divided into two parts,the sorted part at the left end and the unsorted part at the right end.Intially,the sorted part is empty and the unsorted part is the entire list.

STEP BY STEP PROCEDURE OF THE EXPERIMENT:

#include <stdio.h>
int a[100],n,i,j,k,temp,count=0,pos,swap=0;
void selection_sort()
{
    for(i=0;i<n-1;i++){
        pos = i;
        for(j=i+1;j<n;j++){
            if(a[pos] > a[j]){
                pos = j;
                count ++; }
            else{
                count++; }
        }
        if(pos!=i)
        {
            temp = a[i];
            a[i] = a[pos];
            a[pos] = temp;
            swap++;
        }
        count++;
    printf("\nPass %d :\t",i+1);
    for(k=0;k<n;k++){
        printf("%d\t",a[k]);
    }}
}
int main()
{
    printf("Enter the number of elements : ");
    scanf("%d",&n);
    for(i=0;i<n;i++)
    {
        printf("Enter number : ");
        scanf("%d",&a[i]);
    }
    selection_sort();
    printf("\n\nSorted list in ascending order :\n");
    for(i=0;i<n;i++){
        printf("%d ",a[i]);
    }
    return 0;
}

1.Set the min to the experiment.
2.Search the minimum element in the array.
3.Swap the first location with the minimum value in the array.
4.Assign the second element as min.
5.Repeat the process until we get a sortd array.

OutputObtained:

![Test Image](19WH1A12A6-selectionsort output)

![19WH1A12A6-selectionsort output](https://user-images.githubusercontent.com/69143855/93011870-067f1200-f5b8-11ea-82f6-58a78f7ab11e.png)


