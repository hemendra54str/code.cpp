#include<iostream>
using namespace std;
int binarySearch(int arr[],int size,int key){
int s=0;
int e=size-1;
int mid=(s+e)/2;
    while(s<=e){
        if(key==arr[mid]){
            return mid;
        }
        else if(key>arr[mid]){
            s=mid+1;
        }
        else if(key<arr[mid]){
            e=mid-1;
        }
        mid=(s+e)/2;
    }
    return -1;
}
int main(){
    int arr[10]={1,2,3,4,5,6,7,8,9,10};
    int ans=binarySearch(arr,10,5);
    cout<<ans;
    return 1;
}
