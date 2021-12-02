<p align="center">

  <a href="https://github.com/OurForce2020/OpenOasis-Docs">
  <img src="Resources/Logo/logo.svg" alt="OpenOasis-Docs">  
  </a>

</p>

---------------------------------------------------------------------------------

# 开源绿洲 - 文档

简体中文 | [English](README_EN.md)

作为 **开源绿洲（OpenOasis）** 的子项目，主要收集整理涉及流体力学、热力学及碳轨迹相关课题的资料，以及数值计算方案。  
同时，**文档** 包括一些项目协同规范、代码开发规范以及相关技术手册等资料。

+ [项目协同开发方案](#项目协同开发方案)
+ [项目模块算法手册](#项目模块算法手册)
+ [数值计算方案](#数值计算方案)
+ [水文学概要](#水文学概要)
+ [水力学概要](#水力学概要)
+ [热力学概要](#热力学概要)
+ [碳循环理论](#碳循环理论)
+ [其他资源](#其他资源)

---------------------------------------------------------------------------------

## 项目协同开发方案

*Collaborative Development Schemes* 

**开源绿洲** 项目协同开发方案，包括模块开发流程与代码规范等相关资料。

+ [项目协同方案](OpenOasisTutorial/ModuleDevelopeProcess.md)
+ [项目架构](OpenOasisTutorial/OpenOasisFramework.md)
+ [代码规范](OpenOasisTutorial/CodeGuideLines.md)

---------------------------------------------------------------------------------

## 项目模块算法手册

*Module Algorithm Manuals*

**开源绿洲** 项目模块技术手册，包括模块算法原理说明、实现方案，模块使用方法等内容。

### 水文过程模块

+ [单位线产汇流模型](FluidFlow/Hydrology/modules/api.md)
+ [新安江产流模型](FluidFlow/Hydrology/modules/xaj.md)
+ [马斯京根汇流模型](FluidFlow/Hydrology/modules/msk.md)

### 水力过程模块

+ [标准纳维-斯托克斯模型](FluidFlow/Hydraulics/modules/StandardNavierStokesModel.md)
+ [标准圣维南模型](FluidFlow/Hydraulics/modules/StandardSaintVenantModel.md)
+ [标准玻尔兹曼模型](FluidFlow/Hydraulics/modules/StandardBoltzmannModel.md)

### 热流动模块

+ []()

### 碳流动模块

+ []()

---------------------------------------------------------------------------------

## 数值计算方案

*Computing Methods*

数值计算方案文档，主要内容包括主流数值计算算法以及传统方程分析方法。

+ [特征线方法](NumericalComputationMethods/CharacteristicsMethod.md)
+ [瞬时流态法](NumericalComputationMethods/SpecifiedTimeIntervalMethod.md)
+ [有限差分法](NumericalComputationMethods/FiniteDifferenceMethod.md)
+ [有限体积法](NumericalComputationMethods/FiniteVolumeMethod.md)
+ [有限元方法](NumericalComputationMethods/FiniteElementMethod.md)
+ [粒子流体法](NumericalComputationMethods/PatricleHydrodynamicsMethod.md)
+ [深度学习法](NumericalComputationMethods/DeepLearning.md)

---------------------------------------------------------------------------------

## 水文学概要

*Hydrology Synopsis*

水文学概要，主要介绍水文学主要概念及理论基础。

+ [水文学原理](FluidFlow/Hydrology/HydrologicPrinciple.md)

---------------------------------------------------------------------------------

## 水力学概要

*Hydraulics Synopsis*

水力学概要，主要介绍水力学（流体力学）主要概念、理论基础。

+ [纳维-斯托克斯方程组-1](FluidFlow/Hydraulics/NavierStokesEquations.md)
+ [纳维-斯托克斯方程组-2](FluidFlow/Hydraulics/NavierStokesEquations-2.md)
+ [纳维-斯托克斯方程组-3](FluidFlow/Hydraulics/NavierStokesEquations-3.md)
+ [圣维南方程组-1](FluidFlow/Hydraulics/SaintVenantEquations.md)
+ [圣维南方程组-2](FluidFlow/Hydraulics/SaintVenantEquations-2.md)
+ [玻尔兹曼方程组](FluidFlow/Hydraulics/BoltzmannEquations.md)
+ [管网水力学](FluidFlow/Hydraulics/PipeNetwork.md)

---------------------------------------------------------------------------------

## 热力学概要

*Thermodynamics Synopsis*

热力学概要，主要介绍热力学主要概念及理论基础。

+ [热力学原理](HeatFlow/ThermodynamicsPrinciple.md)

---------------------------------------------------------------------------------

## 碳循环理论

*Carbon Cycle Theory*

碳循环理论，主要介绍自然及城市的碳流动过程及规律。

+ [碳循环理论](CarbonFlow/CarbonCycleTheory.md)

---------------------------------------------------------------------------------

## 其他资源

*Resources*

其他资源，主要包括相关专业书籍、相关算例、行业发展报告等资料。

+ [资源](Resources/ReadMe.md)

---------------------------------------------------------------------------------