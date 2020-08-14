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

1.The first element in the array is 3 and the last element is 98
2.mid = sum of first and last indices and divided by 2
3.here mid = 9/2 = 4.5 that is equal to 4
4.a[4] = 36 that is greater than our value 12
5.hence high value becomes mid-1 that is 4-1 is 3
6.now again mid = 3/2 = 1.5 that is equal to 1
7.the element matches with the our required value 12

###Output Obtained

![Test Image](program2output1.png)
![Test Image](program2output2.png)
![Test Image](program2output3.png)

![program2output1](https://user-images.githubusercontent.com/69143855/90255327-c0704a80-de61-11ea-987f-01107849d8bb.png)








