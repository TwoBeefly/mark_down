﻿# 逻辑回归的代价函数
## 代价函数
       为了训练逻辑回归模型的参数w和参数b，需要一个代价函数，通过训练该函数得到w和b
* 逻辑回归的输出函数：      
       $\hat{y}^{(i)}=\sigma(w^Tx^{(i)}+b)$  
       令$z^{(i)}=w^Tx^{(i)}+b$    
       $\sigma(z)=\frac{1}{1+e^{-z}}$

  其中i表示x，y，z第i个训练样本

## 损失函数
       损失函数又叫做误差函数，来衡量预测输出值和实际值有多接近。
* 逻辑回归的损失函数(要尽可能的小))：
$L(\hat{y},y)=-[y\log\hat{y}+(1-y)\log(1-\hat{y})]$     
$\because\hat{y}\in[0,1]$   
$\therefore$ 若y等于1，$L=-y\log\hat{(y)}$，要使L尽可能小，则$\hat{y}$要大，所以$\hat{y}$无限接近于1       
同理，y等于0，$L=-\log(1-\hat{y})$,此时$\hat{y}$无限接近于0

**代价函数对m个样本的损失函数求和然后除以m：**
* $J(w,b)=-\frac{1}{m}\sum_{i=1}^m[y\log\hat{y}+(1-y)\log(1-\hat{y})]$
***