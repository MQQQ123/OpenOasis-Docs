<p align="center">
  <a href="https://github.com/OurForce2020/OpenOasis"><img src="../Resources/Logo/logo.png" alt=""></a>
</p>

---------------------------------------------------------------------------

## Boltzmann Equation

*玻尔兹曼方程*  

<div align="center">  

流体在物理上是大量粒子（10^23量级）构成的离散系统，每个分子作无规则热运动，通过频繁的碰撞来交换动量和能量。    
流体的微观运动具有不均匀性、离散性和随机性，其宏观运动一般总呈现处均匀性、连续性和确定性。  
流体的宏观运动和其他性质是流体分子微观运动的平均结果。  
因此，基于不同的观察尺度，描述流体运动的数学模型（微观分子模型、介观动理模型和宏观连续模型）也会有很大不同。

**微观分子模型**，视流体为大量分子构成的多体系统，分析各流体分子的动力学行为，采用统计方法描述流体整体运动情况。  
**宏观连续模型**，视流体为无数流体质点构成的连续介质体，分析流体微团，通过一组偏微分方程直接描述流体的宏观运动。  

**介观动理模型**，分析流体分子的速度分布函数，通过研究该函数的时空演化过程同时根据宏观物理量与分布函数之间关系，  
获得流体的宏观流动信息。  
与微观模型的共同处在于，都是从微观角度考察流体分子的运动；不同处在于，二者分别描述分子的统计行为、个体行为；  
与宏观模型的共同处在于，二者刻画对象都是微观分子的统计量；不同处在于，前者没有**连续性假设**而后者须以此为前提。

*计算流体力学的学习，明其全而析其微。*

“明其全”，要对所学的数值方法在原理上有较透彻的掌握；“析其微”，要对采用的数值方法在实施中的细节有较深入的了解。

</div>

---------------------------------------------------------------------------

### Macroscopic Continuous Model

*宏观连续模型*

<div align="center"> 

衡量连续介质假设是否合理的特征参数是 **努森数（Knudsen Number）**，即分子平均自由程与流动的宏观特征长度之比：
$$K_n = \frac{\lambda}{L}$$

$\lambda$ 可以理解为分子在两次连续碰撞之间的平均飞行距离；$L$ 通常取为流场或物体的尺寸，或者采用密度的梯度 $L = \frac{\rho}{|\Delta \rho|}$。  
只有当努森数很小时（一般< 0.001），流体才可以视为是连续的。

基于连续介质假设，流体运动遵循质量、动量和能量的守恒定律： 
+ $$\begin{aligned}
\frac{\partial \rho}{\partial t} + \nabla(\rho \textbf{u}) &= 0 \\
\Rightarrow \frac{\partial \rho}{\partial t} + (\frac{\partial \rho u_x}{\partial x} + \frac{\partial \rho u_y}{\partial y} + \frac{\partial \rho u_z}{\partial z} ) &= 0
\end{aligned}$$

+ $$\begin{aligned}
\frac{\partial (\rho \textbf{u})}{\partial t} + \nabla \cdot (\rho \textbf{u} \textbf{u}) &= \nabla \cdot \pmb{\sigma}  \\
\Rightarrow \textbf{x-axis}: \space \frac{\partial \rho u_x}{\partial t} + u_x\frac{\partial \rho  u_x}{\partial x} + u_y\frac{\partial \rho u_x}{\partial y} + u_z\frac{\partial \rho u_x}{\partial z} &= \rho f_x - \frac{\partial p}{\partial x} + \eta (\frac{\partial^2 u_x}{\partial x^2} + \frac{\partial^2 u_x}{\partial y^2} + \frac{\partial^2 u_x}{\partial z^2}) \\
\end{aligned}$$

+ $$\begin{aligned}
\frac{\partial (\rho e)}{\partial t} + \nabla \cdot (\rho e \textbf{u}) \thinspace &= \pmb{\sigma} : \nabla \textbf{u} - \nabla \cdot \textbf{q} \\
\Rightarrow \frac{\mathrm{d} \rho e_s}{\mathrm{d} t} &= \rho \textbf{f}_m \cdot \textbf{u} + \nabla (\textbf{f}_s \cdot \textbf{u}) + \nabla^2 (\kappa T) + \rho \textbf{q}
\end{aligned}$$



其中，$\rho, u, e$ 分别为流体的密度、速度和单位质量的内能，$\sigma$ 为流体的应力张量，$q$ 为由热传导和热辐射引起的热通量。

</div>

---------------------------------------------------------------------------

### References

*参考文献*

[1] 郭照立, 郑楚光. 格子Boltzmann方法的原理及应用[M]. 科学出版社, 2008.     

---------------------------------------------------------------------------

### Authors

*作者*

[1] **朗月**，“ 希望这篇文章能够为你提供帮助，如有错误望不吝指正，欢迎交流！:D ”  

---------------------------------------------------------------------------



