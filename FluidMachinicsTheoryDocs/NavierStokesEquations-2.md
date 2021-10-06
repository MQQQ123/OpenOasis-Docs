<p align="center">
  <a href="https://github.com/OurForce2020/OpenOasis"><img src="../Resources/Logo/logo.png" alt=""></a>
</p>

---------------------------------------------------------------------------------

# 纳维-斯托克斯方程组

*Navier Stokes Equations 2*  

<div align="center">

本篇主要是继续介绍在纳维-斯托克斯模型框架下的流体力学现象和理论。

+ [边界层](#边界层)
+ [平面恒定势流](#平面恒定势流)
+ [量纲分析](#量纲分析)

</div>


---------------------------------------------------------------------------------

## 边界层

*Boundary Layer*

<div align="center">

$$\begin{cases}
u_x\frac{\partial u_x}{\partial x} + u_y\frac{\partial u_x}{\partial y} = - \frac{1}{\rho}\frac{\partial p}{\partial x} + \nu \frac{\partial^2 u_x}{\partial y^2}  \\
  \\
\frac{\partial p}{\partial x} = 0 \\
  \\
\frac{\partial u_x}{\partial x} + \frac{\partial u_y}{\partial y} = 0 \\
\end{cases}$$
 
分析边界层的微分方程组，可以知道：  
+ 边界层内压强沿 y 方向不变并等于边界层外边界上的压强；边界层外边界上压强可由势流理论求解，内部压强可知；
+ 惯性项和粘性项既均不能省略，则应有相同的数量级，$\frac{U_{0}^{2}}{l} \sim \nu \frac{U_0}{\delta^2} \quad \Rightarrow \frac{\delta}{l} \sim \frac{1}{\sqrt{R_{el}}}, \quad R_{el} = \frac{U_0 l}{\nu}$;
+ 边界层的厚度 $\delta$ 与绕流物体长度 $l$ 的比值的数量级，是以该物体长度表示的雷诺数平方根的倒数 ；
+ 方程虽基于平面绕流推导，但一般可用于曲率较小的曲面边界层：此时，取固体表面曲线为 x 轴，曲线法向为 y 轴。

<img src="./Imgs/60.jpg" width=210 height=200>
<img src="./Imgs/61.jpg" width=210 height=200>
<img src="./Imgs/62.jpg" width=210 height=200>

依据边界层的概念，可将流体分为两个区域：边界层内的粘滞流动和边界层外的理想流体势流流动。一般情况下，  
将固体表面沿法线方向分布的流速达到 99%U0 之处视作边界层外边界。

**流量损失厚度**，实际流体流经固体壁面时，边界层内通过的流量比理想流体在同一范围内的流量要小；所以设想 ，  
若将固体边界以上一个厚度为 $\delta_1$ 的水层排除，则在 $\delta - \delta_1$ 厚度内通过的流量与实际流体在边界层内的流量相等；  
$\delta_1$ 即为流量损失厚度，又称排挤厚度。

可得边界层内单宽流量以及流量方程 ：  
$$
q = \int_{0}^{\delta} u_x \mathrm{d}y = U_0(\delta - \delta_1) = \int_{0}^{\delta} U_0 \mathrm{d}y - U_0 \delta_1  \qquad \Rightarrow \quad \delta_1 = \int_{0}^{\delta} (1 - \frac{u_x}{U_0}) \mathrm{d} y
$$

**总动量损失厚度**，由于固体边界对流体的阻滞作用，边界层内通过的流体动量比理想流体情况下要小；所以设想 ，  
将固体边界上排除一个厚度为 $\delta^{*}$ 的水层，则在 $\delta - \delta^{*}$ 厚度内通过的流体动量与实际流体在边界层内的动量相等；  
$\delta^{*}$ 即为总动量损失厚度，而其实际又可以分为两部分组成：
1. 由于流量损失造成的动量损失，厚度为 $\delta_1$;
2. 由于边界层内流速分布所造成的动量损失，厚度为 $\delta_2$，一般称为 **动量损失厚度**。

可得边界层内单宽动量及动量方程 ：  
$$\begin{gathered}
M = \int_{0}^{\delta} \rho u_{x}^{2} \mathrm{d} y = \rho U_{0}^{2} (\delta - \delta^{*}) = \int_{0}^{\delta} \rho U_{0}^{2} \mathrm{d}y - \rho U_{0}^{2} \delta^{*} \quad \Rightarrow  \delta^{*} = \int_{0}^{\delta} (1 - \frac{u_{x}^{2}}{U_{0}^{2}}) \mathrm{d} y \\
\Rightarrow \quad \delta_2 = \delta^{*} - \delta_1 = \int_{0}^{\delta} \frac{u_x}{U_0} (1 - \frac{u_x}{U_0}) \mathrm{d} y
\end{gathered}$$

**总能量损失厚度**，由于固体边界对流体的阻滞作用，边界层内通过的流体能量比理想流体情况下要小；所以设想 ，  
将固体边界上排除一个厚度为 $\delta^{**}$ 的水层，则在 $\delta - \delta^{**}$ 厚度内通过的流体能量与实际流体在边界层内能量相等；  
$\delta^{**}$ 即为总能量损失厚度，而其实际又可以分为两部分组成：
1. 由于流量损失造成的能量损失，厚度为 $\delta_1$;
2. 由于边界层内流速分布所造成的能量损失，厚度为 $\delta_3$，一般称为 **能量损失厚度**。

可得边界层内单宽能量及能量方程 ：  
$$\begin{gathered}
E = \int_{0}^{\delta} \frac{\rho u_{x}^{3}}{2} \mathrm{d} y = \frac{\rho U_{0}^{3}}{2} (\delta - \delta^{**}) = \int_{0}^{\delta} \frac{\rho U_{0}^{3}}{2} \mathrm{d} y - \frac{\rho U_{0}^{3}}{2} \delta^{**} \Rightarrow \delta^{**} = \int_{0}^{\delta} (1 - \frac{u_{x}^{3}}{U_{0}^{3}}) \mathrm{d} y \\
\Rightarrow \quad \delta_3 = \delta^{**} - \delta_1 = \int_{0}^{\delta} \frac{u_x}{U_0} (1 - \frac{u_{x}^{2}}{U_{0}^{2}}) \mathrm{d} y
\end{gathered}$$

*------------------ * ------------------*

<img src="./Imgs/63.jpg" width=420 height=200>

流体绕固体边界流动形成一层很薄的边界层，取出其中一微分控制体 ABCD 。其中，AB 为离边界起点 x 处断面，  
CD 断面离边界起点 x+dx，该两断面无限接近，则该段边界层底边 BD 视为直线。  
将坐标系的原点取在固体表面切线上，y 轴垂直于固体表面。  

B 点边界层的厚度为 $\delta$，D 点处边界层的厚度为 $\delta + \frac{\partial \delta}{\partial x} \mathrm{d} x$；  
边界层上每点的流速一般不是一个常数，但因 AC 的长度是一个无限小量，故认为其上流速均等于 A 点流速 $U_0$ 。

单位时间内通过 AB 断面的单宽流量质量：  
$$\rho q = \rho U_0 (\delta - \delta_1)$$

单位时间内通过 AB 断面的单宽质量动量：  
$$M = \rho U_{0}^{2} (\delta - \delta^{*}) = \rho U_{0}^{2} (\delta - \delta_1 - \delta_2)$$

若流体不可压缩，单位时间内流出 CD 断面的质量 $\rho q + \frac{\partial \rho q}{\partial x} \mathrm{d} x$；质量守恒，通过外边界 AC 流入质量 $\rho \frac{\partial q}{\partial x} \mathrm{d} x$ 。
在时段 $\mathrm{d}t$ 内自断面 AB 流入的动量为 $M \mathrm{d} t$，自断面 CD 流出的动量$M \mathrm{d}t + \frac{\partial M}{\partial x} \mathrm{d}x\mathrm{d}t$；$\mathrm{d}t$ 时段内动量变化为： 
$$\Delta M = (M + \frac{\partial M}{\partial x} \mathrm{d}x) \mathrm{d}t - M \mathrm{d}t - (\rho U_0 \frac{\partial q}{\partial x} \mathrm{d}x) \mathrm{d}t = \frac{\partial M}{\partial x} \mathrm{d}x \mathrm{d}t - \rho U_0 \frac{\partial q}{\partial x} \mathrm{d}x \mathrm{d}t$$

再来讨论在时段 dt 内作用在控制体 ABCD 上外力在流动方向的冲量，所受到的外力有：
+ 作用在断面 AB 上的动水压力；
+ 作用在断面 CD 上的动水压力；
+ 作用在外边界 AC 上的动水压力在流动方向上的分量；
+ 作用在固体边界 BD 上的源自其固体表面的摩擦阻力。

因为在边界层内同一断面上的动水压强相等，令 AB 断面上压强为 $p$，则在 CD 断面上压强为 $p + \frac{\partial p}{\partial x} \mathrm{d} x$；则有，  
$$I_{AB} = p \delta \mathrm{d}t, \quad I_{CD} = (p + \frac{\partial p}{\partial x} \mathrm{d} x) (\delta + \frac{\partial \delta}{\partial s} \mathrm{d}x) \mathrm{d}t
$$

外边界上水流为势流，若不计重力（势能），其能量方程为 $\frac{p}{\rho g} + \frac{U_{0}^{2}}{2 g} = const$；因为外边界上流速可视为常数，  
故外边界 AC 上动水压强也为常数，均等于 A 点动水压强p。由此，作用在外边界上动水压力在流动方向上分量：  
$$p [(\delta + \frac{\partial \delta}{\partial x} \mathrm{d}x) - \delta ] = p \frac{\partial \delta}{\partial x} \mathrm{d}x \quad \Rightarrow I_{AC} = p \frac{\partial \delta}{\partial x} \mathrm{d}x \mathrm{d}t
$$

若作用在固体表面的切应力为 $\tau_0$，则作用在固体表面 BD 上的摩擦阻力的冲量为:  
$$I_{BD} = \tau_0 \mathrm{d}x \mathrm{d}t$$

因此，在时段 dt 内作用在整个控制体 ABCD 上的外力在流动方向的综合冲量为：  
$$I = I_{AB} + I_{AC} - I_{CD} - I_{BD} = - \delta \frac{\partial p}{\partial x} \mathrm{d}x \mathrm{d}t - \tau_0 \mathrm{d}x \mathrm{d}t$$

可得控制体上的动量方程： 
$$- \delta \frac{\partial p}{\partial x} \mathrm{d}x \mathrm{d}t - \tau_0 \mathrm{d}x \mathrm{d}t = \frac{\partial M}{\partial x} \mathrm{d}x \mathrm{d}t - \rho U_0 \frac{\partial q}{\partial x} \mathrm{d}x \mathrm{d}t $$

代入 q，M 的表达式可得：  
$$-\frac{\tau_0}{\rho}-\frac{\delta}{\rho} \frac{\partial p}{\partial x} = - U_{0}^{2} \frac{\partial \delta_2}{\partial x} + (\delta - \delta_1 - \delta_2) U_0 \frac{\partial U_0}{\partial x}$$

因为 $p + \frac{\rho U_{0}^{2}}{2} = const$， 对两边微分则可以得到 $\frac{1}{\rho} \frac{\partial p}{\partial x} = - U_0 \frac{\partial U_0}{\partial x}$ ，代入上式中可以得到 **边界层的动量方程**：  
$$\frac{\tau_0}{\rho U_{0}^{2}} = \frac{\partial \delta_2}{\partial x} + (2 \delta_2 + \delta_1) \frac{1}{U_0} \frac{\partial U_0}{\partial x}$$

由于未对 $\tau_0$ 作任何限制，故方程对于层流、湍流均适用。

当极薄平板顺流放置于无限平行直流中，因为平板和边界层厚度均极薄，可以认为平板不影响边界层以外的液流； 
因此，边界层外的边界上每点的流速及动水压强均将为常数，即 $\frac{\partial p}{\partial x} = 0, \frac{\partial U_0}{\partial x} = 0$ 。所以，对于平板边界层有 ：  
$$\frac{\tau_0}{\rho U_{0}^{2}} = \frac{\mathrm{d} \delta_2}{\mathrm{d} x}$$

对于平板层流边界层，通常假设 $\tau$ 在整个边界层内沿法向线性变化；由此，得到层内流速分布、厚度和阻力公式。  
对于平板湍流边界层，通常假设管流与边界层厚度等于管半径的流动等价，以管道湍流流速和$\tau_0$ 公式求解边界层。

*------------------ * ------------------*

<img src="./Imgs/64.jpg" width=280 height=200>
<img src="./Imgs/65.jpg" width=320 height=200>

分析流体绕圆柱体流动的情况：  
在驻点 N 处压强最大，流体受到较强压力而发生转向流向圆柱体两侧；同时，由于柱面的阻滞作用形成边界层。   

从 N 点起向下游 A 或 B 点前，因圆柱面的弯曲，流体受挤压、流速沿程增加，故外边界上 $\frac{\partial U_0}{\partial x} > 0, \frac{\partial p}{\partial x} < 0$ ；  
即，在 NA 或 NB 段内流体增速减压；该段边界层内通过压强下降弥补能量损失，同时一部分压能转化为动能 。  
流体到达 A 或 B 点时压强减小至最低，流速增大到最大。

从 A 或 B 点往下游，由于圆柱面弯曲，流体扩散、流速沿程减小，$\frac{\partial U_0}{\partial x} < 0, \frac{\partial p}{\partial x} > 0$；边界层是减速增压状态。  
边界层流体越往下游流速越小，直至 C 点，流速减至 0 而停止前进；C 点以下，主流离开曲面以减缓流体扩散 ，  
同时下游流体随机填补空出区域并形成旋涡，称为 **边界层的分离**。

在**分离点** C 形成的旋涡随流带走，由于流体的粘滞性，旋涡在经过一段距离后逐渐衰减消失、旋涡能量转为热能，
其能量损失称为 **旋涡损失**，相应的阻力称为 **旋涡阻力** 。

通过边界层理论分析可知，流体对绕流物体的阻力可以看作是两部分组成：固体表面的摩擦阻力和流体旋涡阻力 。  
流体在物体表面上的摩擦力在水流向的投影即摩擦阻力：  
$$F_f = C_f A_f \frac{\rho U_{0}^{2}}{2}$$

$A_f$ 通常为切应力作用的投影面积；$C_f$ 为表面阻力系数。

由于物体尾部由旋涡发生以致物体表面的压强分布不对称，使水流方向由压差产生，这部分压强阻力即旋涡阻力：  
$$F_p = C_p A_p \frac{\rho U_{0}^{2}}{2}$$

$A_p$ 为垂直流速方向的迎流投影面积；$C_f$ 压强阻力系数。

<img src="./Imgs/66.jpg" width=620 height=240>

若令 $C_d = C_f + C_p$ 为绕流阻力系数；一般的，对于圆柱体绕流：  
1. 当 Re 很小时，边界层属于层流，绕流阻力仅有摩擦阻力，尚无旋涡产生；Cd 与 Re 成反比；
2. 随 Re 增大，圆柱尾部产生旋涡，绕流阻力由摩擦阻力和压强阻力两部分构成；
3. 当 Re 增至 1e4 时，压强阻力时主要的；
4. 当 Re 增至 3e5 时，因为此时圆柱体表面的边界层由层流开始转变为湍流，所以Cd 突然下降。

湍流边界层内流速比层流时大，所以湍流边界层分离点的位置较层流时更接近尾部；层流转为湍流时Cd 减小。

</div>


[home](#纳维-斯托克斯方程组)

*--- 本章作者：---*

[1] **朗月**，“ 希望这篇文章能够为你提供帮助，如有错误望不吝指正，欢迎交流！:D ” 

*--- 参考资料：---*

[1] 吴持恭. 水力学：下册[M]. 高等教育出版社, 2007. 

---------------------------------------------------------------------------------

## 恒定平面势流

*Two-Dimensional Steady Potential Flow*

<div align="center">

 

</div>

[home](#纳维-斯托克斯方程组)

*--- 本章作者：---*

[1] **朗月**，“ 希望这篇文章能够为你提供帮助，如有错误望不吝指正，欢迎交流！:D ” 

*--- 参考资料：---*

[1] 吴持恭. 水力学：下册[M]. 高等教育出版社, 2007. 

---------------------------------------------------------------------------------

## 量纲分析

*Dimensional Analysis*

<div align="center">

 

</div>

[home](#纳维-斯托克斯方程组)

*--- 本章作者：---*

[1] **朗月**，“ 希望这篇文章能够为你提供帮助，如有错误望不吝指正，欢迎交流！:D ” 

*--- 参考资料：---*

[1] 吴持恭. 水力学：下册[M]. 高等教育出版社, 2007. 

---------------------------------------------------------------------------------
