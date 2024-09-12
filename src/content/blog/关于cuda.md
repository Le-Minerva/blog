---
author: Le-Minerva
pubDatetime: 2024-09-13T03:10:52Z
modDatetime: 2024-09-13T03:10:52Z
title: 关于cuda
slug: 关于cuda
featured: true
ogImage: https://user-images.githubusercontent.com/53733092/215771435-25408246-2309-4f8b-a781-1f3d93bdf0ec.png
tags:
  - cuda
description: 关于cuda的一些基本知识
---

# 关于cuda

GPU特别擅长处理图像数据，而CUDA（Compute Unified Device Architecture），是显卡厂商NVIDIA推出的运算平台。CUDA™是一种由NVIDIA推出的通用[并行计算](https://zhida.zhihu.com/search?q=并行计算&zhida_source=entity&is_preview=1)架构，该架构使GPU能够解决复杂的计算问题。它包含了CUDA指令集架构（ISA）以及GPU内部的并行计算引擎，安装cuda之后，可以加快GPU的运算和处理速度，还有一个叫做cudnn，是针对深度卷积神经网络的加速库

**什么是显卡？**

显卡（Video card，Graphics card）全称显示接口卡，又称显示适配器，是计算机最基本配置、最重要的配件之一。显卡作为电脑主机里的一个重要组成部分，是电脑进行数模信号转换的设备，承担输出显示图形的任务。显卡接在电脑主板上，它将电脑的数字信号转换成模拟信号让显示器显示出来，同时显卡还是有图像处理能力，可协助CPU工作，提高整体的运行速度。对于从事专业图形设计的人来说显卡非常重要。民用和军用显卡图形芯片供应商主要包括AMD(超微半导体)和Nvidia(英伟达)2家。现在的top500计算机，都包含显卡计算核心。在科学计算中，显卡被称为显示加速卡。

**什么是显存？**

也被叫做[帧缓存](https://zhida.zhihu.com/search?q=帧缓存&zhida_source=entity&is_preview=1)，它的作用是用来存储显卡芯片处理过或者即将提取的渲染数据。如同计算机的内存一样，显存是用来存储要处理的图形信息的部件。

**CUDA和cuDNN的安装**

如果我们想要下载安装CUDA需要有NVIDA的显卡、Windows系统、Visual Studio，因为CUDA在安装时，需要VS的里面的工具包来编译

在CUDA安装完之后，如果想要学习深度学习中的神经网络的话，则额外下载安装cuDNN，可帮助我们加快神经网络的运算，cuDNN是一个常见的神经网络层加速库文件，能够很大程度把加载到显卡上的网络层数据进行优化计算，而CUDA就像一个很粗重的加速库，其主要依靠的是显卡。cuDNN需要在有CUDA的基础上进行，可以在CUDA基础上加速2倍以上

**注意：**cuDNN是一个SDK，是一个专门用于神经网络的加速包，它跟我们的CUDA没有一一对应的关系，即每一个版本的CUDA可能有好几个版本的cuDNN与之对应，但一般有一个最新版本的cuDNN版本与CUDA对应更好。

**CuDNN支持的算法**

- 卷积操作、相关操作的前向和后向过程
- pooling的前向后向过程
- softmax的前向后向过程
- 激活函数的前向后向过程,如（Relu、Sigmoid、Tanh ）等