---
date:
  created: 2023-12-31
---

# Happy new years eve!

We hope you are all having fun and wish you all the best for the new year!
<!-- more -->

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua.


# 测试公式

$$\frac{1}{2}mv^2+J\dot{\phi}^2-mgG(\phi)$$

$$
\dot{N}+[\Omega,N]=0.
$$

\begin{equation}
\dot{N}+[\Omega,N]=0.
\tag{1}\label{sample}
\end{equation}

公式 \eqref{sample}


In equation \eqref{eq:sample}, we find the value of an
interesting integral:

\begin{equation}
  \int_0^\infty \frac{x^3}{e^x-1}\,dx = \frac{\pi^4}{15}
  \label{eq:sample}
\end{equation}

```julia
f(x)=x^2+12
for i in eachindex(0:0.1:2pi)
    f(i)
end
```

Euler 盘是一个很有意思的教学玩具, 它大概在上世纪九十年代被发明 (命名为 Euler 盘是为了纪念 Euler, 有条件的读者可以查看维基百科), 随后变成了一个较为流行的教学工具. Euler 盘是一个较重的, 扁的圆柱形的铁盘, 另外还有一个光滑的镜面, 使 Euler 盘可以在镜面上旋转. 不同于一个硬币只能在桌子上旋转几秒钟, 一个精心制作的 Euler 盘甚至能旋转 8 分钟, 可参看这个[视频](https://www.bilibili.com/video/BV14P4y177xW/?spm_id_from=333.337.search-card.all.click). 

下面我们将用理论力学的知识对 Euler 盘进行动力学建模, 并使用 Mathematica 求解微分方程, 可视化其运动.

由于 Euler 盘与镜面都是比较光滑的, 在建模时很自然地假设接触点的速度是水平的, 即接触点可以滑动. 然而在文献 \cite{petrie2002} 中的实验发现, 接触点至少在前期重心位置较高的时候没有滑动, 而是作纯滚动. 因此我们也将采用纯滚动这个假设. 如果读者想参考纯滑动的模型, 可参见我的手写稿 [Euler Disk](/files/Euler%20Disk.pdf). 考虑这样一个纯滚动的特例的难度, 与考虑任意刚体在水平面的纯滚动问题的难度没有太大区别, 因此我们将先考虑后者, 而后再特例化, 回到我们的模型.

\section{运动微分方程}
我们假设读者已经熟悉了刚体动力学的知识, 包括惯性张量, 角速度, 角动量, Euler 角等概念以及它们之间的联系. 这些知识可以在国内的任一本高等动力学教材中找到, 如果读者想看较为数学化的阐述, 可参考 Arnold 的经典教材: 经典力学的数学方法, 也可参看我的读书笔记: [刚体动力学](/files/rigid-body-dynamics1.pdf).

