Aim of the Experiment: Write a program to sort elements by using bubble sorting technique.


Description of Bubble sorting:It is also refers as sinking sort,is a simple sorting algorithm that repeatdely steps through the list, compares adjacent elements and swaps them if they are in the wrong order.The pass through the list is repeated until the list is sorted.


Step-by-step procedure of the experiment:

#include<stdio.h>
int main()
{
    int array[100],n,i,j,swap;
    printf("enter no. of elements: ");
    scanf("%d", &n);
    printf("enter %d numbers: ", n);
    for(i= 0; i< n; i++)
    {
    scanf("%d", &array[i]);
    }
    for(i = 0; i<n-1;i++)
    {
        for(j=0; j< n-i-1; j++)
        {
            if(array[j] > array[j+1])
            {
                swap = array[j];
                array[j]=array[j+1];
                array[j+1]= swap;
            }
        }
    }
    printf("sorted array:\n");
    for(i = 0; i<n; i++)
    {
    printf("%d\n", array[i]);
    }
    return 0;
}


1.In this first part of the code we accept the number of terms in the array and store it in n.
2.Then we enters the elements of the array.
3.Then there are two 'for loops'.
4.the first 'for loop' runs from 1 value to zero all the way till it is less than n-1.
5.The outer array takes care of the element of the value to be compared to all the other elements.
6.Inside the for loop ,there is another for loop that starts from j=0 all the way to j<n-i-1.
7.This loop takes care of all elements.Inside,there  is an if statement that compares if a[j] > a[j+1].
8.If this condition is satisfied then swapping takes place.
9.First, a[j] is assigned to swap,followed by a[j+1] being assigned at a[j] and at last swap is assigned to a[j+1].
10. this continues till all the elements are sorted


Output Obtained:

![Test Image](DS bubble output)

![DS bubble output](https://user-images.githubusercontent.com/69143855/91007725-52164f80-e5fa-11ea-9db3-9ea79ee8e1a1.png)
