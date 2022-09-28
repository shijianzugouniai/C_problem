n个整数,前面的数字往后移m个位置,后面M个的数字变成前面M个的数字

```c
/**
移动的思路为:每往后面移动一次,循环递归m次
*/
void move(int *p,int n,int m){ // n个数字,移动m位
  int fast,last;// 两个指针分别指向最前面和最后面
  int i;
  last=*(p+n-1);
  int *index=p+n-1;// index先指向最后
  for(int i=0;i<n-1;i++){
    // 从后往前赋值
      *(index-i)=*(index-i-1);
      
 }  
  
      // 移动到第一个停止，将最后一个赋值给首位
      *p=last;
    // 需要移动M次，M为0时停止递归
    m--;
    if(m>0) move(p,n,m)    
 }
int main(){
  void(int *p,int n,int m);
  int num[20];
  printf("想要多少个数:\n");
  int N;
  scanf("%d",&N);
  printf("ok 输入%d个数字:\n");
 int i;
 for(int i=0;i<N;i++){
     scanf("%d",&num[i]);
     
 }   
 printf("需要后移几位:");
 int m;
 scanf("%d",&m);
 move(num,N,m);
 printf("移动%d位的结果:",m);   
 for(int i=0;i<N;i++){
     printf("%d",num[i]);
 }   
   printf("/n"); 
 }






```

 
