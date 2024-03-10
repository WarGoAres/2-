# 2-
2分搜尋
#include <stdio.h>
//2分搜尋(要先排序)
//演算法時間O(lgn)
int binarysearch(int a[],int findnumber,int left,int right){

  int middle;//中
  
  middle=(left+right)/2;
  
  if(left>right){
      
    return -1;  
  }    
  
  if(a[middle]==findnumber){
      
     return  middle; 
      
  }
    
    
    
   if(a[middle]>findnumber){
      
      
    return binarysearch(a,findnumber,left,middle-1);  
      
  }  
    
  
  else{
      
      
    return binarysearch(a,findnumber,middle+1,right);  
      
  }  
    
  
  
  
  
  
    
    
}


int main(void)
{
 


    int a[] = {76, 82, 97, 98, 100};
    printf("Binary Search Result: %d\n", binarysearch(a, 100, 0, 4)); //2分搜尋的結果
    return 0;
 

    
}
 







