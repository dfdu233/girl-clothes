# girl-clothes
all pictures on girl clothes
#include<stdio.h>
using namespace std;
struct js{
	int to;
};
int main(){
   js sz[105]={0};
   int num;
   int k,m,temp;
   scanf("%d%d%d",&num,&k,&m);
   for(int i=1;i<=num-1;i++){
   	    sz[i].to=i+1;
   }
   sz[num].to=1;
   temp=k;
   bool pd[101]={0};
   for(int i=1;i<=num-2;i++){
   	      //  printf("temp=%d",temp);
			for(int j=1;j<=m-2;j++){
   	     	    temp=sz[temp].to;
			}//find 
			// printf("sz[temp]=%d",sz[temp]);
             pd[sz[temp].to]=1;
			 sz[temp].to=sz[sz[temp].to].to;
			 temp=sz[temp].to;
             
             //delete
   }//delete all
   for(int i=1;i<=num;i++){
   	  if(pd[i]==0)printf("%d ",i);
   }
   
    int a;
    return 0;
}
