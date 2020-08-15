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

Output1(key element = 36):
we check each element of the given array against the given key element = 36.
when the search reaches fifth element,the element in the array matches with the key element,hence the search ends here.Thus the position(index) of the element is obtained that is equal to 4.we got the required output.

Output2(key element = 100):
we check the each element of the given array against the given key element = 100.
The search reaches the last element of the array but as no element in the array matches with the element in the array,the search ends here.The search is unsuccessful as the element is not present.Hence it displays that the element is not found.


###Output Obtained

![Test Image1](Program 1 output 1.png)
![Test Image2](program 1 output 2.png)

![program 1 output 1](https://user-images.githubusercontent.com/69143855/90199478-86b42b00-ddf2-11ea-984e-5bc450f6c2ca.png)

![program 1 output 2](https://user-images.githubusercontent.com/69143855/90199702-24a7f580-ddf3-11ea-8aee-0a5c01b4e72a.png)


