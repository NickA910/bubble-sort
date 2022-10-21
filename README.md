# bubble-sort
#include <iostream>

using namespace std;
int *bubblesort (int besararray, int arraynya[]){
    int a,b,simpen;
    a= besararray -1;
    for (int i = a; i>0; i--){
        for (int j = a; j>0; j--){
            b= j -1 ;
            if (arraynya[j] < arraynya[b]){
                simpen = arraynya[j];
                arraynya[j] = arraynya[b];
                arraynya[b] = simpen;
            }
            
        }
    }
    return arraynya;
}

int main()
{
    const int besar = 5;
    int cari, *hasil;
    int array1[besar];
    cout << "masukan data angka sebanyak " << besar << " untuk disortir: ";
    for (int i=0; i<besar; i++){
        cin >> array1[i];
    }
 
    hasil = bubblesort(besar, array1);
    cout << "hasilnya setelah di sort adalah: ";
    for (int j=0; j<besar; j++){
        cout << hasil[j] << " ";
    }
    return 0;
}
