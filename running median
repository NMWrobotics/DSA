#include <iostream>
#include <vector>
using namespace std;

void swap(int* a, int* b) {
    int t = *a;
    *a = *b;
    *b = t;
}

int partition(int arr[], int low, int high) {
    int pivot = arr[high];
    int i = low - 1;

    for (int j = low; j <= high - 1; j++) {
        if (arr[j] <= pivot) {
            i++;
            swap(&arr[i], &arr[j]);
        }
    }
    swap(&arr[i + 1], &arr[high]);
    return (i + 1);
}

void quickSort(int arr[], int low, int high) {
    if (low < high) {
        int pi = partition(arr, low, high);
        quickSort(arr, low, pi - 1);
        quickSort(arr, pi + 1, high);
    }
}


int main(){

    int arr[6] = {7,3,5,2,6,9};
    int n = 6;
    int newarr[4];
    float median = 0;
  /*  cout<<"enter array";
     for (int i = 0; i < n; i++){
        cin >> arr[i];
    } */
    cout << "sorted"<< "\t\t"<< "median"<<endl;

     for (int i = 0; i<= n-1; i++){
            newarr[i] = arr[i];
            
             
             quickSort(newarr, 0, i);
             for (int j = 0; j<= i; j++){
                    cout<<newarr[j]<<" ";
             }
             if ((i+1) %2 == 0) {
                //cout<<"even";
                //cout<< i;
                median = (float(newarr[i/2]) + float(newarr[(i/2)+1])) / 2;
                cout <<"\t\t"<< median;
                
             }else{
                median = float(newarr[i/2]);
                cout <<"\t\t"<< median;

             }
             cout<<endl; 


    

     }





}
