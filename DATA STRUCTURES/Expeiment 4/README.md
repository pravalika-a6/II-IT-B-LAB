#Experiment 4
##Aim of the experiment -  write a program to search an element in an array by using binary searching recursive method.
##Description of binary search - Binary search also known as half-interval search,logarithmic search is a search algorithm that finds the position of a target value within a sorted array.Binary search compares the targeted value to the middle element of the array.
###Step-by-step procedure of the experiment
#include<stdio.h>
int recbinarysearch(int array[],int low,int high,int value)
{
    if(high > low)
    {
        int mid = low + (high-low)/2;
        if(array[mid] == value)
        {
            return mid;
        }
        if(array[mid] > value)
        {
            return recbinarysearch(array,low,mid-1,value);
        }
        return recbinarysearch(array,mid+1,high,value);
    }
    return -1;
}
int main(void)
{
    int array[] = {3,12,29,33,36,54,60,61,92,98};
    int i,value;
    for(i=0;i<10;i++)
    {
        printf("%d",array[i]);
    }
    int n = sizeof(array)/sizeof(array[0]);
    printf("enter the values\n");
    scanf("%d",&value);
    int result = recbinarysearch(array,0,n-1,value);
    if(result == -1)
    {
        printf("element is not present in the array");
    }
    else
    {
        printf("%d found at %d",value,result);
    }
    return 0;
    
}

1.The first element in the array is 3 and the last element is 98
2.mid = sum of first and last indices and divided by 2
3.here mid = 9/2 = 4.5 that is equal to 4
4.a[4] = 36 that is greater than our value 12
5.hence high value becomes mid-1 that is 4-1 is 3
6.now again mid = 3/2 = 1.5 that is equal to 1
7.the element matches with the our required value 12

###Output Obtained

![Test Image](pro2output1.png)
![Test Image](pro2output2.png)
![Test Image](pro2output3.png)
