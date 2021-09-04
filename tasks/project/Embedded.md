# 单片机题 简易信号发生器

## 1 简要描述
使用普通单片机（Arduino，stm32，msp430等，不推荐使用51单片机），采用直接数字合成技术（DDS），制作一个频率幅度可调的信号发生器。

选择此题目需要自己准备材料。包括单片机，0.96寸OLED屏幕，1602LCD，数模转换模块，旋钮编码器，杜邦线等。本题除了需要上交代码外，还需要现场评测。

## 2 具体要求

### 2.1 产生信号
- 能够产生20Hz-2kHz的正弦波
- 能够产生20Hz-4kHz的三角波
- 能够产生20Hz-1MHz的方波
- 能够产生自定义的波形

要求四种波形都能实现频率和幅度的可调。

### 2.2 控制逻辑
能够用**一个**旋转编码器，完成频率调节，幅度调节与波形切换三个功能
- 左旋或右旋编码器，可以完成频率或幅度可调
- **单击**旋转编码器，完成频率和幅度调节的切换
- **双击**旋转编码器，完成波形的切换

### 2.3 显示
规定使用0.96寸的OLED，对当前输出的波形信息进行显示
- 波形的类型
- 波形的频率
- 波形的峰峰值
- 波形的大致形状

### 2.4 波形输出
自制 或 购买 数模转换模块完成单片机产生的数字信号到示波器观测的模拟信号的转换。评测时，将用示波器观测输出的信号。

测评现场必须看到实际波形。

### 2.5 与上位机通信（进阶要求）
在电脑上通过画图软件画出简单的单次信号波形，设计UI界面，将波形通过该UI界面以某种数据格式上传存储至单片机。上传成功后，数据掉电后不会丢失。单片机能读取该数据，并且将该存储的信号周期输出。


## 3 评分细则
### 3.1 基本要求
占比75%。
#### 波形输出
- 能输出频率幅度可调正弦波 得分20%
- 能输出频率幅度可调三角波 得分10%
- 能输出频率幅度可调方波 得分10%
#### 旋钮编码器的控制
- 实现单击检测 得分5%
- 实现左旋右旋检测 得分8%
- 实现双击检测 得分12%
#### OLED显示
- 实现波形的各种参数的显示（见2.3）得分10%

### 3.2 进阶要求
占比25%。
- 实现一个“波形下载”的UI界面 得分10%
- 实现波形的周期复现，且频率幅度可调 得分15%

## 4 学习资料
- 学习单片机的原理与应用。
    - 建议没有单片机基础的同学学习 Arduino，比较容易入门。
    - 参考资源：[Arduino中文社区](https://www.arduino.cn/)、[STM32官方参考手册和数据手册](https://www.stmcu.com.cn/Designresource/design_list/cat_code/document/pro_cat/STM32/is_first/1)、[正点原子的《STM32开发指南》电子书](http://www.stmcu.org/module/forum/forum.php?mod=viewthread&tid=615919)、bilibili 上的入门教程。
- 学习 Arduino / STM32 基础编程，安装 Arduino IDE / Keil5。（可在 Windows 上玩）
- 掌握单片机系统架构，学习 GPIO、中断、定时器、PWM、串口通信、I2C 通信、SPI 通信的原理与应用。（如果对单片机还不熟悉，推荐按照这个顺序学习。）
- 学习使用外设，如 LED 灯、按键、OLED 显示屏等。学会查阅英文芯片数据手册。
- 学习 STM32 单片机的需要了解标准库。