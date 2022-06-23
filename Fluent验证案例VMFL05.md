Fluent验证案例：VMFL-05

- *Poiseuille Flow in a Pipe<sup>[1]</sup>*.
*(直管中的泊肃叶定律）*

## 00.案例描述

### Physics/Model

- Steady laminar flow

### Test case
>Fully developed laminar flow in a circular tube is modeled. Reynolds number based on the tube diameter
is 500. Only half of the axisymmetric domain is modeled.

![Figure .04.1:Flow Domain](images/vm-image05/1.jpg)

### Conditions

Material Properties | Geometry | Boundary Condition
--------------------|----------|-------------------
Density = 1 kg/m<sup>3</sup> | Length of the pipe =1.5 m | Fully developed laminar velocity profile at inlet with an average velocity of 2.00 m/s
Viscosity =1e-5 kg/m<sup>-s</sup> | Radius of the pipe =0.00125 m | 

### Analysis Assumptions and Modeling Notes
The flow is steady. A fully developed laminar velocity profile is prescribed at the inlet. Hagen-Poiseuille equation is used to determine the pressure drop analytically.



### Goal

+ 获取直管层流流动时进出口压降值，与解析值进行比较

## 01.二维建模

![SCDM中: 二维模型及边界命名](images/vm-image05/2.jpg)

## 02.网格划分

![Mesh: 网格划分-整体](images/vm-image05/3.jpg)

如果还需要调整一下网格的分布（沿着径向方向的疏密程度），可以采取如下操作：

![Mesh: 网格划分-“中心密，两端疏”](images/vm-image05/4.jpg)

## 04.Fluent设置

![Fluent参数设置要点](images/vm-image05/5.jpg)

***注意***：对于入口速度，定义为充分发展的层流流动速度分布($\overline{V}=2m/s$)。

![Fluent参数设置要点-Inlet速度在径向方向分布的关系式](images/vm-image05/7.jpg)


## 05.计算结果

### 5.1 Results Comparison for ANSYS Fluent

  | Target | Target |ANSYS Fluent | Ratio
  :-------:|:-------------:|:---------:|:----:
  Pressure | 10.24  | 10.22 | 0.998

### 5.2 Practical results

![Plot: Velocity](images/vm-image05/8.jpg)

![计算结果对比](images/vm-image05/9.jpg)



- 本文案例（VM-05）获取：https://pan.baidu.com/s/1kAgk5VmF2bZbd_kNZsljzQ 
提取码：qq28



*参考资料*

>[1] ANSYS Fluid Dynamics Verification Manual. 2020:19-20.