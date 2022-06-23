Fluent验证案例：VMFL-08

- *Non-Newtonian Flow in a Pipe<sup>[1]</sup>*.
*(旋转腔体流动计算）*

## 00.案例描述

### Physics/Model

- Laminar flow, Rotating reference frame

### Test case

> Flow in a cylindrical cavity enclosed with a lid that spins at Ω = 1.0 rad/s. The flow field is 2–D axisymmetric, so only the region bounded by the dashed lines in Figure .08.1: Flow Domain (p. 25)needs to be modeled. The Reynolds number of the flow based on the cavity radius R and the tip-speed of the disk is 1800.

![Figure .08.1:Flow Domain](images/vm-image08/1.jpg)

### Conditions

| Material Properties | Geometry | Boundary Condition |
| :--------------------: |:----------:|:-------------------:|
| Density = 1 kg/m <sup>3</sup> | Height of the cavity = 1 m | Speed of rotation of the moving wall = 1 rad/s |
| Viscosity: 0.000556 kg/m<sup>-s</sup> | Radius of cavity = 1 m | Rotational velocity for cell zone = -1 rad/s |



### Analysis Assumptions and Modeling Notes

The flow is laminar. The problem is solved using rotating reference frame.


### Goal

+ 观测某一截面上的速度分布，与目标值进行比较

## 01.二维建模

![SCDM中: 二维模型及边界命名](images/vm-image08/2.jpg)

## 02.网格划分

![Mesh: 网格划分情况](images/vm-image08/3.jpg)

## 04.Fluent设置

![Fluent参数设置要点](images/vm-image08/4.jpg)


## 05.计算结果

### 5.1 Results Comparison

![Comparison of Distribution of Radial Velocity Along a Section at Y= 0.6 m](https://mmbiz.qpic.cn/mmbiz_png/RUUZenibQFtbkibQicxRLppV7Bq9umiaticaiabaLpTibibsF3mW7ibXYHSkicGG8KZ6ia7wZKX24oJibA2TfWc530EqJWtZWw/0?wx_fmt=png)

![Comparison of Distribution of Swirl Velocity Along a Section at Y= 0.6 m](images/vm-image08/5.jpg)

### 5.2 Practical results

![Distribution of Radial Velocity](images/vm-image08/6.jpg)

![Distribution Swirl Velocity](images/vm-image08/7.jpg)

- 本文案例（VM-08）获取：https://pan.baidu.com/s/1ARMiMQDM0mScFER7xNtKQw 提取码：mb85 

*参考资料*

>[1] ANSYS Fluid Dynamics Verification Manual. 2020:25-28.<br>
