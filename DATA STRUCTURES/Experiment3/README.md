#Experiment 3

##Aim of the experiment -  write a program to search an element in an array by using binary searching iterative method.

##Description of binary search - Binary search also known as half-interval search,logarithmic search is a search algorithm that finds the position of a target value within a sorted array.Binary search compares the targeted value to the middle element of the array.

###Step-by-step procedure of the experiment

#include<stdio.h>
int binarysearch(int[],int,int,int);
int main()
{
    int i,key,position;
    int a[10] = {3,12,29,33,36,54,60,61,92,98};
    scanf("%d",&key);
    position = binarysearch(a,0,10,key);
    if(position == -1)
    {
        printf("element is not found");
    }
    else
    {
        printf("%d found at %d",key,position);
    }
    return 0;
}
int binarysearch(int a[],int first,int last,int key)
{
    int mid;
    while(first <= last)
   {
        mid = (first + last)/2;
        if(a[mid] == key)
        {
            return mid;
        }
        else if(key > a[mid])
        {
            first = mid+1;
        }
        else
        {
            last = mid-1;
        }
    }
    return -1;
}





