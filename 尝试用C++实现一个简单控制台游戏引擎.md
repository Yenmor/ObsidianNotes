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

# 创建可供复用的 Screen 对象
- Screen 对象应包含以下属性
	- width 游戏屏幕的宽度
	- height 游戏屏幕的高度
	- vector<char> data 屏幕中每个像素的数据
	-  vector<GameObject*> objs 在屏幕上的游戏物体
	-  pixel_count 屏幕的像素数量，就是 width*height

<br>

- Screen 对象应包含以下方法
	- addObj() 向 Screen 对象中添加一个游戏物体
	- draw() 根据 Screen 中存在的游戏物体在控制台上绘制Screen
	- update() 更新 Screen 状态和内部游戏物体的状态
	- writeObj() 在 Screen 上绘制游戏物体的方法，基本属于内部方法

>你或许要问 addObj() 和 writeObj() 的区别
>addObj()只负责将游戏物体添加到 Screen 内部的游戏物体列表
>writeObj() 则真正的将游戏物体画到屏幕的像素信息上，大多数时候writeObj() 该被当作内部方法