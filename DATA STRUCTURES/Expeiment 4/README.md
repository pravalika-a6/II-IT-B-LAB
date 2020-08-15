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

Output1(key element = 12)
1.The first element in the array is 3 and the last element is 98
2.mid = sum of first and last indices and divided by 2
3.here mid = 9/2 = 4.5 that is equal to 4
4.a[4] = 36 that is greater than our key value 12
5.hence high value becomes mid-1 that is 4-1 is 3
6.now again mid = 3/2 = 1.5 that is equal to 1
7.then a[1] = 12,that matches with our key element 12
8.Hence we obtained our required element.

Output2(key element = 92)
1.The first element in the array is 3 and the last element is 98
2.mid = sum of first and last indices and divided by 2
3.here mid = 9/2 = 4.5 that is  equal to 4
4.a[4] = 36 that is smaller than our key value 92
5.Hence the low value becomes mid+1 that is equal to 5
6.Now again mid = 14/2 that is equal to 7
7.then a[7] = 60,that is smaller than our key value 92
8.hence again the low value becomes mid+1 that is equal to 8
9.now again mid = 17/2 =  = 8.5 = 8
10.then a[8] = 92,that is equal to our key value
11.thus the position of 92 gets printed
12.Hence we obtained our required element.

Output3(key element = 33)
1.The first element in the array is 3 and the last element is 98
2.mid = sum of first and last indices and divided by 2
3.here mid = 9/2 = 4.5 that is  equal to 4
4.a[4] = 36, that is greater than our key value 33
5.hence the high value becomes mid-1 = 4-1 = 3
6.Again mid = 3/2 = 1.5 = 1
7.a[1] = 12 that is lesser than our required value i.e 33
8.then our low value = mid+1  = 1+1 = 2
9.now mid = 2+3/2 = 2.5 = 2
10.a[2] = 29,smaller than 33
11.hence low value = mid+1 = 2+1 = 3
12.a[3] = 33,that is equal to our required value
13.Hence we obtained our required element.

###Output Obtained

![Test Image](pro2output1.png)
![Test Image](pro2output2.png)
![Test Image](pro2output3.png)


![pro2output1](https://user-images.githubusercontent.com/69143855/90243360-65802880-de4c-11ea-98c1-b25060bc29ca.png)

![pro2output2](https://user-images.githubusercontent.com/69143855/90243937-6a91a780-de4d-11ea-8c3c-548a50ba863b.png)

![pro2output3](https://user-images.githubusercontent.com/69143855/90244194-e855b300-de4d-11ea-860a-39a05b6cd977.png)





