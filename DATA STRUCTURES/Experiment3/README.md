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
12.Hence we odtained our required element.

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
13.Hence we obtained our required value.


###Output Obtained

![Test Image](program2output1.png)
![Test Image](program2output2.png)
![Test Image](program2output3.png)

![program2output1](https://user-images.githubusercontent.com/69143855/90255327-c0704a80-de61-11ea-987f-01107849d8bb.png)
![program2output2](https://user-images.githubusercontent.com/69143855/90255696-42f90a00-de62-11ea-8ff0-73012b168b4a.png)
![program2output3](https://user-images.githubusercontent.com/69143855/90255751-56a47080-de62-11ea-8ef0-913f1ce62cd1.png)







