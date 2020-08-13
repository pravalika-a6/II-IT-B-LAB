#Experiment 1
##Aim of the experiment -  write a program to search an element in an array by using linear searching iterative method
##Description of linear search - A linear search or sequential search is amethod for finding an element within a list. It sequentially checks each element of the list until a match is found or the whole list has been searched.
###Step-by-step procedure
#include<stdio.h>
int linearsearch(int array[],int size,int value)
{
    for(int i=0;i<size;i++)
    {
        if(array[i] == value)
        {
            return i;
        }
    }
    return -1;
}
int main(void)
{
    int array[] = {12,61,33,92,36,3,29,98,54,60};
    int key = 36;
    int size = 10;
    int result = linearsearch(array,size,key);
    if(result == -1)
    {
        printf("element not found");
    }
    else
    printf("%d is present at index %d",key,result);
    return 0;
}
1.an array of ten elements is given
2.And the value to be find is also given
3.the first element is 12,it doesnot matches with the value
4.so we check the second,third and so on until the element matches with the value
5.the fifth element 36 matches with the value. so, the index of thet number will get printed
6.we get the required solution

###Output Obtained

![Test Image1](Program 1 output 1.png)
![Test Image2](program 1 output 2.png)

