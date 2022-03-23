------------------------------------------------------------------------------------------------------------------------------------------------

# Minecraft_using_python

-------------------------------------------------------------------------------------------------------------------------------------------------

--##--This is a purely python oriented minecraft game. Not much as of real but its fun.

-------------------------------------------------------------------------------------------------------------------------------------------------

--##--This is the base for the evoluiton of minecraft like games.

-------------------------------------------------------------------------------------------------------------------------------------------------

-----------------------------------------------------------------DISCUSSING ABOUT IN GAME FEATURES-----------------------------------------------

--##--You will have controll on the following keys in your keyboard:

                                                     __
                                        --##--'W'------|
                                                       |
                                        --##--'S'------|
                                                       |------ Character Movement
                                        --##--'A'------|
                                                       |
                                        --##--'D'------|
                                                     __|
                                                     
                                                     
                                                     __
                                        --##--'1'------|
                                                       |
                                        --##--'2'------|
                                                       |
                                        --##--'3'------|
                                                       |
                                        --##--'4'------|
                                                       |
                                        --##--'5'------|------ Switch between diffrent textures of blocks.
                                                       |
                                        --##--'6'------|
                                                       |
                                        --##--'7'------|
                                                       |
                                        --##--'8'------|
                                                       |
                                        --##--'9'------|
                                                     __|
                                                     
                                        --##--'Space Bar'----- Character Jump

-------------------------------------------------------------------------------------------------------------------------------------------------

--##--Also you muust have your controll on your mouse :

                                        --##--'Right Click' ---- Place Blocks on the place 
                                        
                                        --##--'Left Click' ---- Remove Blocks from the place 
-------------------------------------------------------------------------------------------------------------------------------------------------

################## IMPORTANT NOTE #####################

"""""A NEW FEATURE OF FLYING HAS BEEN ADDED JUST LIKE THE ELYTRA IN MINECRAFT WHICH WILL BE FUN TO USE AS IT ALSO PREVENTS YOU FROM FALLING AFTER THE ENTITY .....

--##-- ALL YOU JUST NEED TO DO IS PRESS 'TAB' KEY AND AIM THE MOUSE AT THE POINT WHERE YOU WANT TO FLY AND PRESS MOVEMENT KEYS.

--##-- 'LEFT SHIFT' IS FOR SPRINTING

--##-- 'LEFT CTRL' IS FOR CROUCHING
                                        
-------------------------------------------------------------------------------------------------------------------------------------------------

The play zone is confined . If you fall apart, !!  FLY FLY TO REACH HOME  !!

-------------------------------------------------------------------------------------------------------------------------------------------------

--##--Comment me if there are any queries....

-------------------------------------------------------------------------------------------------------------------------------------------------

--##--Please do follow me on GitHub for more.

-------------------------------------------------------------------------------------------------------------------------------------------------

----------------------------------------------------------HAPPY GAMING WITH  PYTHON---------------------------------------------------------------






#include <stdio.h>
void insert(int a[],int p,int e){
    int n;
    n=sizeof(a);
    for(int i=n;i>=p;i--){
        a[i+1]=a[i];}
        a[p]=e;
        n=n+1;
}
void del(int a[],int p){
    int n;
    n=sizeof(a);
    for(int i=p;i<n;i++){
        a[i]=a[i+1];}
        n=n-1;
}
void display(int a[]){
    int n;
    n=sizeof(a);
    printf("");
    for(int i=0;i<=n;i++){
        printf("%d ",a[i]);
    }printf("\n");
}
void search(int a[],int e){
    int n,b,flag;
    n=sizeof(a);
    for(int i=0;i<=n;i++){
        if(e==a[i]){
            flag=1;
            b=i;
            break;
        }
    }
    if(flag==1){
        printf("Found at %d\n",b);
    }
    else{
        printf("Not found");
    }printf("\n");
}
void sortarray(int a[]){
    int temp,length = sizeof(a);
    for (int i = 0; i < length; i++) {     
        for (int j = i+1; j < length; j++) {     
           if(a[i] > a[j]) {
               temp = a[i];    
               a[i] = a[j];    
               a[j] = temp;    
           }     
        }     
    }
    for (int i=0; i<length; i++) {     
        printf("%d ", a[i]);    
    }
}
int main(){
    int arr[10]={1,2,3,4,5},c,p,e,x;
    x=1;
    while(x){
        printf("\n1.Insert\n2.Delete\n3.Display\n4.Search\n5.Sort\n6.Exit\n\nEnter your choice : ");
        scanf("%d",&c);
        switch(c){
            case 1:
                printf("Enter position : ");
                scanf("%d",&p);
                printf("Enter element : ");
                scanf("%d",&e);
                insert(arr,p,e);
                printf("Inserted\n");
                break;
            case 2:
                printf("Enter position : ");
                scanf("%d",&p);
                del(arr,p);
                printf("Deleted");
                break;
            case 3:
                display(arr);
                break;
            case 4:
                printf("\nEnter Value : ");
                scanf("%d",&e);
                search(arr,e);
                break;
            case 5:
                sortarray(arr);
                break;
            case 6:
                x=0;
                printf("Thank you");
                break;
        }
    }
}
