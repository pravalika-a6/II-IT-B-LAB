#Experiment 2

##Aim of the experiment - write a program to search an element in an array by using linear searching recursive method.

##Description of linear searching - A linear search or sequential search is a method for finding an element within a list.It sequentially checks each element of the list until a match is found or the whole list has been searched.

###Step-by-step procedure of the experiment

#include<stdio.h>
int reclinearsearch(int array[],int value,int index,int n){
    int s = 0;
    if(index >= n)
    {
        return 0;
    }
    else if (array[index] == value){
        s = index + 1;
    }
    else{
        return reclinearsearch(array,value,index+1,n);
    }
    return s;
}
int main(){
    int n,i,value,s;
    int array[100];
    printf("enter the total  no of elements");
    scanf("%d", &n);
    for(i=0;i<n;i++)
    {
        scanf("%d",&array[i]);
    }
    printf("enter the elements to search");
    scanf("%d",&value);
    s = reclinearsearch(array,value,0,n);
    if(s != 0)
    {
        printf("element found at s %d",s-1);
    }
    else{
        printf("element not found");
    }
    return 0;
    



###Output Obtained

![Test Image](program 1 output 1.png)
![Test Image](program 1 output 2.png)

![program 1 output 1](https://user-images.githubusercontent.com/69143855/90199478-86b42b00-ddf2-11ea-984e-5bc450f6c2ca.png)

![program 1 output 2](https://user-images.githubusercontent.com/69143855/90199349-1a392c00-ddf2-11ea-874f-51c4a7b30ea8.png)









