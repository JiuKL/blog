[TOC]

# Basics of Neural Network Programming



## Logistic Regression

given x , want  $\hat{y}=P(y=1|x)$, $x\in\R^{n_x}$ 

> $\hat{y_1}=w_{11}*x_{11}+w_{12}*x_{12}+\dots+w_{1n_x}*x_{1n_x}+b_1$.

Parameters:   $w\in\R^{n_x}, b\in\R$

Output:   $\hat{y}=\sigma(w^T+b),\ \ \ \hat{y}\in(0,1)$.

> $\sigma(z)=\cfrac{1}{1+e^{-z}}$.



Loss(error) function: 

$\ell(\hat{y},y)=\cfrac{1}{2}(\hat{y}-y)^2$,    $\ell(\hat{y},y)=-(y\log\hat{y}+(1-y)\log(1-\hat{y}))$.

> $\log\lrArr \ln$.
>
> For the second function, if $y=1,\ell(\hat{y},y)=-y\log \hat{y}$ and you want loss function close 0, $\hat{y}$ must be as big as possible. As we all know $\hat{y}\in(0,1)$, so when $y=1.\ \ell(\hat{y},y)\rarr 0$, $\hat{y}$ will be close 1.



Cost function: 

$\begin{aligned}J(w,b)&=\cfrac{1}{m}\displaystyle\sum_{i=1}^{m}\ell(\hat{y}^{(i)},y^{(i)})\\&=-\cfrac{1}{m}\displaystyle\sum_{i=1}^{m}\bigg[y^{(i)}\log\hat{y}^{(i)}+(1-y^{(i)})\log(1-\hat{y}^{(i)})\bigg]\end{aligned}$.



Gradient descent algorithm:

$\begin{aligned}Repeat&\{\\w :&= w-\alpha\cfrac{dJ(w)}{dw}\\&\}\end{aligned}$.

> ignore parameter b: $J(w,b)\rarr J(w)$.
>
> $\alpha$ : learning rate


p