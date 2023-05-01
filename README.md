#include<stdio.h>
#include<stdlib.h>
#define max 5

typedef struct node{

int arr[max];
int front;
int rear;
}st;


void create(st *ptr);
void enqueue(st *ptr);
void dequeue(st *ptr);
void isfull(st *ptr);
int main(){
st Node;
st *ptr;
ptr=&Node;
int ans;
int vela;
do{
printf("\t\t\t01.Create\n");
printf("\t\t\t02.Enque\n");
printf("\t\t\t03.Deque\n");
printf("\t\t\t04.Is_full\n");
printf("\t\t\t05.Is_Empty\n");
printf("\t\t\t06.Display\n");
printf("\t\t\t00.Exit\n\n\n");

printf("Enter Your Choice:");
scanf("%d",&ans);
switch(ans){

case 1:
create(ptr);
break;

case 2:
enqueue(ptr);
break;

case 3:
dequeue(ptr);
break;
case 4:
isfull(ptr);
break;
case 5:
//enque();
break;
case 6:
//enque();
break;
case 0:
exit(0);
break;
default:
printf("Wrong Choice Try Again...\n");
}
printf("Do you wants to Continue if \n\n\tYES[press any number without 0] \n\tNO[0]: ");
scanf("%d",&vela);
}while(vela!=0);
return 0;}

void create(st *ptr){

ptr->front=0;
ptr->rear=0;
printf("The Queue is Ready to Use...\n\n");

}void enqueue(st *ptr){

printf("\nEnter Your Value :");
scanf("%d",&ptr->arr[ptr->rear]);

printf("The value %d Was Successfully Added...\n",ptr->arr[ptr->rear]);
ptr->rear++;
}void dequeue(st *ptr){

printf("The Value %d was Removed...\n",ptr->arr[ptr->front]);
ptr->front++;

}void isfull(st *ptr){

if(((ptr->front==0)&&(ptr->rear==max-1))||(ptr->front>=ptr->rear)){
printf("The Queue Is Full...");

}else{
printf("The QUEUE is not fill... \n");}

}
