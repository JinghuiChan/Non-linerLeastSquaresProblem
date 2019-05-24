# Non-liner Least Squares Problem
#### Key word: Ceres  g2o   Gauss-Newton
---

## 问题描述:  
#### 设有曲线满足以下方程：    
#### y = e<sup>(ax<sup>2</sup>+bx+c)</sup>+w    
#### 其中，a,b,c为曲线参数，w为噪声。现有N个数据点(x,y)，希望通过此N个点来拟合a,b,c。实验中取N = 100.    
####  那么，定义误差 e<sub>i</sub> = y<sub>i</sub> - e<sup>(ax<sup>2</sup><sub>i</sub>+bx<sub>i</sub>+c)</sup>,于是(a,b,c)的最有解可通过解以下最小二乘获得：  
 
![avatar](https://github.com/JinghuiChan/Non-linerLeastSquaresProblem/blob/master/optimization.png)
