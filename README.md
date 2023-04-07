# CTDL-GT_Exponential_Recursion_1.cpp
Exponential Recursion
Nguồn tham khảo : https://codehow.net/de-quy-da-tuyen-exponential-recursion-trong-c-c++-90.html
*  Cai đặt : 

+ Hàm đệ quy đa tuyến (Exponential Recursion) là một hàm mà khi chúng ta gọi đệ quy, 
nó sẽ phát sinh ra thêm n lần đệ quy khác. 
Hiểu đơn giản hơn thì một hàm có n lần đệ quy trong thân hàm gọi là hàm đệ quy đa tuyến.

*  Ví Dụ : 

+ Chúng ta có một hàm đệ quy đa tuyến dưới đây. Hàm này có chức năng tìm dãy nhị phân có chiều dài n : 

void daTuyen(int i, int n, int *X)
{
    int val;    
    for (val = 0; val < 2; val++)
    {
        X[i] = val;
        if (i == (n-1))      
        {
            int j;
            for(j = 0; j < n; j ++)     
            {
                cout<< X[j];
            }
            cout<<"\n";
        }
        else         
        {
            daTuyen(i+1, n, X); 
        }
    }
}
