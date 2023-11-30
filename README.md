# 第二次任务

## 学习外部中断 串口 定时器

用usb转ttl模块，使用定时器，初始状态为每100ms串口上传“mode 1 100ms”，并使用按键+外部中断，每进入一次外部中断，发送时间加100ms，同时修改上传的数据包（如进入一次外部中断，则每200ms上传“mode 2 200ms”）

***
## 代码介绍
以上为本次单片机任务的内容，以下为我的代码解决方案的介绍：\
本次代码基于**STM32F103C8T6**单片机，单片机的部分IO口配置是PA0-PA7是LED0-LED8，输出模式，初始电位是高电平,PB12-PB14是KEY0-KEY2,输入模式，其他IO口的配置可以打开**STM32CubeMX**生成的.**ioc**文件查看，使用STM32CubeMX生成配置文件，通过**Hal**库编程，使用**Clion**编译和烧录。
电路板图片如下：

<div  align="center">    

<img src="./docs/circuit.jpg" width="50%" height="50%">

</div>

所有任务均在这个代码里面实现，具体切换在**main.h**中的宏定义用户代码块：
```c
/* USER CODE BEGIN Private defines */
//#define TASK1
#define TASK2
//#define TASK3
//#define TASK4
//#define TASK5
/* USER CODE END Private defines */
```
如果想要切换成对应的任务的代码，只需要将对应任务前面的注释去掉，并把其他任务注释掉即可。\
演示如下：\
任务1
![image](./docs/task1%20-small-original.gif)
任务2
![image](./docs/task2%20-small-original.gif)\
任务3
![image](./docs/task3%20-small-original.gif)
任务4
![image](./docs/task4%20-small-original.gif)\
任务5
![image](./docs/task5%20-small-original.gif)\
维护人：袁汉阔\
邮箱：yuanhankuo@qq.com
