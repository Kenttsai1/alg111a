# 期中

## UVA11150 Cola

## 題目敘述

![](https://i.imgur.com/WZ6cSAG.png)

## 使用模擬法

因為三個空瓶可以換一瓶可樂，因此最後只會剩下一個或兩個空瓶。如果剩兩個空瓶時，借一個空瓶可以多喝一瓶可樂，還可以返還一個空瓶。

## 程式碼
``` cpp
#include <iostream>
using namespace std;

int main()
{
	int cola,count;
	
	while(cin >> cola){
		int count = 0;
		
		while(cola >= 3){
			count +=3; //drink 3
			cola -=2; //-2
		}
		
		if (cola == 2)count+=3;
		else count+=cola;
		
	
		cout << count << endl;
	
	}
	return 0;
	
}

```
放一下CHATGPT的解

![](https://i.imgur.com/NEfB9KK.png)
