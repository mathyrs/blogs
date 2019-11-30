## 线性规划基本概念

#### 线性规划标准型

$$\begin{aligned} minimize &  \qquad   \boldsymbol c^T \boldsymbol x \\ subject\quad to&\qquad  \boldsymbol A \boldsymbol x= \boldsymbol b \\ &\qquad  \boldsymbol x  \geq  \boldsymbol 0 \end{aligned}$$

其中，$\boldsymbol A$是$m\times n$实数矩阵，$m<n$, ${\rm rank}\boldsymbol A=m$. 不失一般性，假设$\boldsymbol b \geq \boldsymbol 0$.

任何形式的线性规划问题都可以转换为标准型。

#### 基本解

从$\boldsymbol A$中选择$m$个线性无关的列向量组成方阵$\boldsymbol B$，对$\boldsymbol A$的列向量进行重新排序，可使得$B$中的列向量位于$\boldsymbol A$中的前$m$列，即$A$可写为分块矩阵$\boldsymbol A=[\boldsymbol B,\boldsymbol D]$，其中$\boldsymbol D$是$m\times (n-m)$矩阵，它由$\boldsymbol A$中其余的列向量组成。矩阵$\boldsymbol B$是非奇异的，因此，可求得方程$\boldsymbol B\boldsymbol x_B=\boldsymbol b$的解$\boldsymbol x_B$。令$\boldsymbol x$为$n$维向量，且$\boldsymbol x=[\boldsymbol x^T_B,\boldsymbol 0^T]^T$。那么$\boldsymbol x$是方程$\boldsymbol A\boldsymbol x=\boldsymbol b$的一个解。
$\boldsymbol x=[\boldsymbol x^T_B,\boldsymbol 0^T]^T$是$\boldsymbol A\boldsymbol x=\boldsymbol b$在基$\boldsymbol B$下的**基本解**，向量$\boldsymbol x_B$中的元素成为**基变量**，$\boldsymbol B$中的列向量称为基本列向量。
如果基本解中的某些基变量为零，那么这个基本解称为**退化基本解**。
满足$\boldsymbol A\boldsymbol x=\boldsymbol b,\boldsymbol x \geq \boldsymbol 0$的向量$\boldsymbol x$称为**可行解**。
如果某个可行解也是基本解，那么称之为**基本可行解**。
如果基本可行解是退化的基本解，那么称之为**退化的基本可行解**。
#### 线性规划基本定理
对于任何满足约束条件$\boldsymbol A\boldsymbol x=\boldsymbol b,\boldsymbol x \geq \boldsymbol 0$的向量$\boldsymbol x$，如果它能够使目标函数$\boldsymbol C^T\boldsymbol x$取得最小值，那么就将其称为**最优可行解**。如果最优可行解是基本解，那么称为**最优基本可行解**。
**线性规划定理**：对于线性规划的标准型，有如下两个命题。
1. 如果存在可行解，那么一定存在基本可行解；
2. 如果存在最优可行解，那么一定存在最优基本可行解；

#### 约束集的极点与基本可行解等价

对任何$\boldsymbol x,\boldsymbol y\in \Theta$和任意实数$\alpha, 0<\alpha <1$， 如果有$\alpha \boldsymbol x+(1-\alpha)\boldsymbol y\in \Theta$成立，则称集合$\mathbb{\Theta}^n$为**凸集**

满足约束条件$\boldsymbol A\boldsymbol x=\boldsymbol b,\boldsymbol x \geq \boldsymbol 0$的点集是凸集。

对于凸集$\Theta$内的点$\boldsymbol x$，如果在$\Theta$中找不到两个不同的点$\boldsymbol x_1$和$\boldsymbol x_2$，对于某个$\alpha\in (0,1)$，使得$\boldsymbol x=\alpha \boldsymbol x_1 + (1+\alpha)\boldsymbol x_2$成立，则称$\boldsymbol x$为$\Theta$的极点。

$\Omega$表示由所有可行解组成的凸集，即集合中的所有$n$维向量$x$满足$$\boldsymbol A \boldsymbol x= \boldsymbol b,\qquad  \boldsymbol x  \geq  \boldsymbol 0 $$其中，$A \in \mathbb{R}^{m\times n}, m<n$。那么，$x$是$\Omega$的极点当且仅当$x$是$\boldsymbol A\boldsymbol x=\boldsymbol b,\boldsymbol x\geq \boldsymbol 0$的基本可行解。

#### 参考文献
[1]. Chong E K P , Stanislaw H. Żak. An Introduction to Optimization[J]. IEEE Antennas and Propagation Magazine, 1996, 38(2):60.