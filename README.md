#include <iostream>
using namespace std;

void fun(int a[], int n) {
    int min = a[0];
    int index = 0;
    
    for(int i = 0; i < n; i++) {
        if(a[i] < min) {
            min = a[i];
            index = i;
        }
    }
    
    int temp = a[index];
    a[index] = a[n-1];
    a[n-1] = temp;
}

int main() {
    int a[10], n;
    cout << "输入数组长度: ";
    cin >> n;
    cout << "输入 " << n << " 个数: ";
    for(int i = 0; i < n; i++) {
        cin >> a[i];
    }
    
    fun(a, n);
    
    cout << "结果: ";
    for(int i = 0; i < n; i++) {
        cout << a[i] << " ";
    }
    cout << endl;
    
    return 0;
}
