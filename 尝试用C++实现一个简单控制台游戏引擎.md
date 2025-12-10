***
# 背景：

本人接触过相当一阵子的 java, unity 和 C sharp, 用 pygame 写过一些小游戏，现在要来学C++，便想用制作游戏引擎的方式边做边学。

# 最初的步骤：

选择使用一个字符串来保存整个游戏画面，并每帧调用清屏函数再重绘控制台。
- `#include <cstdlib>` 用来提供清屏函数
- `#define CLEAR system("cls")` 定义清屏函数
- `#include <windows.h>` 提供 Sleep() 函数用于停止线程
> Sleep() 传入的是毫秒数，所以 \*1000  处理 
- 以下程序可以动态输出 screen 中的内容，在 while 循环中对字符串进行修改即可改变屏幕显示
```cpp
#include <windows.h>
#include <cstdlib>
#include <iostream>
#define CLEAR system("cls")

//init
int FPS = 30;
double frameTime = 1.0 / FPS ;
std::string screen = "00000000000 v 00000000000"


int main(){
	while(1){
		CLEAR;
		std::cout << screen
		Sleep((long)(frameTime * 1000));
	}
}
```

