# 期中

## UVA11150 Cola

## 題目敘述

![](https://i.imgur.com/WZ6cSAG.png)

## 使用模擬法

因為三個空瓶可以換一瓶可樂，因此最後只會剩下一個或兩個空瓶。如果剩兩個空瓶時，借一個空瓶可以多喝一瓶可樂，還可以返還一個空瓶。

## 程式碼
``` cpp=
#include <iostream>
using namespace std;

int main()
{
	int cola,count;
	
	while(cin >> cola){
		int count = 0;
		
		while(cola >= 3){
			count +=3; //drink 3
			cola -=2; //喝3 換一瓶 剩餘瓶數-2
		}
		
		if (cola == 2)count+=3; //兩瓶可借一瓶 
		else count+=cola;
		
	
		cout << count << endl;
	
	}
	return 0;
	
}

```
# Result 測資
![](https://i.imgur.com/Ltb8d9T.png)


## 補充一下我問ChatGPT得到的解

這是第一次的程式碼 他是有錯誤的 因此在側資方面沒有通過

```cpp=
#include <iostream>
#include <cstdio>
#include <cstring>
#include <cstdlib>

using namespace std;

int main()
{
    int n;
    while(cin>>n)
    {
        int ans=0;
        while(n>2)
        {
            ans+=n/3;
            n=(n/3)+(n%3);
        }
        if(n==2)
        {
            ans++;
        }
        cout<<ans<<endl;
    }
    return 0;
}


```

但這程式碼是錯誤的 因此我想稍微修改他

但我看不太懂它裡面計算的方式

因此改完後又會回到我上面原本寫的
