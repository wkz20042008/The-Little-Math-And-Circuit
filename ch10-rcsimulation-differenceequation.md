### 电感走起

还记得中学学过的电感不？电感上会累积磁链，而磁链是对电动势的积分，电感上的感应电动势就等于磁链对时间的导数，磁链与电流的比值就是电感，于是我们看下面的电路图

![](/assets/MathCircuit_S2_P4.png)

图4.电感L电路

整个电路电感L的磁链等于Us的积分，电感的电流等于磁链比上电感值，于是得到下面的式子

![](/assets/MathCircuit_S2_E6.png)

在这里电压源Us给电感L充电的电路里，如果一切条件理想化，那电感上的电电流I会一直上升到无穷大，电感越大上升的速度越慢，Us越大，电流上升的速度越快。

如果我们将电压源Us变为电流源Is，同时在回路里加入一个电阻R，如果5所示，现在想问一下，电感L上的电压会怎么变化呢？？

![](/assets/MathCircuit_S2_P5.png)

图5.电感RL电路

是不是看着很像，RC电路，后面的话，就不推导了。其实L与C是一个对偶元件

**电容是：电压的微分对应电流，电流的积分是电压，电压是果，电流是因**

**电感是：电流的微分对应电压，电压的积分是电流，电流是果，电压是因**

### 3.RLC电路

下面我们把一个电感和一个电容连在一起，会发生什么奇妙的现象呢？？？假设电感1mH，初始电流为0，1000uF电容，初始电压为1V，我们直接在Simulink里进行仿真，这个电路会发生什么反应？？？如图6所示

![](/assets/MathCircuit_S2_P6.png)

图6.LC电路仿真图（黄色为电容电压，紫色为电感电流）

电感的电流和电容的电压，都震荡起来了，我去，这是为什么？？？？我们回忆一下上一节我们得到的结论，电容的电压是果电流是因，电感的电压是因电流是果，如果把这俩放一起，那不就是电流与电压互为因果了嘛？？？？互为因果，你推我一把，我又反过来推你一把，不断地推来推去，那不就都震荡起来啦。。。

如果这个LC电路没有任何损耗的话，那这个震荡过程会永远进行下去，如果我们用数学方式描述刚才的过程的话，可以这样进行

![](/assets/MathCircuit_S2_E7.png)

有没有看到最后的这个微分方程，二阶特征方程的，没有实根，纯虚数解，于是高等数学公式一路走起，最后的解是三角函数，这也正好对应了我们之前仿真的震荡。

如果在LC里面加一个0.1欧的电阻呢？？？那又会是如何反应呢？？我们先仿真试一试效果如图7所示。

![](/assets/MathCircuit_S2_P7.png)

图7.RLC仿真图

为什么震荡的幅度不断衰减，越来越小，废话，因为电流流过电阻会消耗能量呀，。。。。每震荡一次，能量就会消耗掉一部分，越来越少

整个RLC如果用微分方程表达的话，那mmmm，我已经不想去算了。。。太麻烦了

