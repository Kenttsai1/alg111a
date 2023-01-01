# 期末

## UVA 11332 Summing Digits

## 題目敘述

![](https://i.imgur.com/TuwOrQ9.png)

# 程式碼 直接運算求解

```
對於所有正整數 n ，我們定義一函數 f(n) 為 n 的每一個十進位數字的總和，
若再把 f(n) 代入函數中可得最到 n,f(n),f(f(n)),f(f(f(n)))… 
最後得到僅有一位數字的值，並定義該值為 g(n) 。
輸入n後，直接丟入迴圈進行算數
```

```cpp!=
#include<iostream>
using namespace std;

int main()
{   
    int n,s; //input sum
    

    while(cin >> n and n!=0)
    {
        while(n>9)  
        {
            s = 0;
            while(n!=0)
            {
                s+=n%10;
                n/=10;

            } 
            n = s;
        }
        cout << n << endl;
    }
    
    
    return 0;


}
```

# Result

![](https://i.imgur.com/0uuPTo4.png)



