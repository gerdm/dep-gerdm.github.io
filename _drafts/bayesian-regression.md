---
mathjax: true
layout: post
title:  "Bayesian Linear Regression"
author: Gerardo Durán Martín
categories: bayes
---

<div style="text-align: center;">
<img src="{{site.url}}/assets/img/download.png">
</div>

TensorFlow 2.0 was announced along with the new TFP library. I cannot overemphasize how excited I was for the news, as I am currently learning the theoretical aspects of bayesian machine learning methods. But after reading their post I was not sure about what where they doing.

Since I am old fashion, I will take it step by step to understand this powerful tool and the consequences it could have to the possible models I might develop.

## Linear Regression and Basis Functions
A regression function is one that maps an $M$-dimensional input vector $\bf x$ to a $k$-dimensional output vector $\bf t$.

In its most simplest form, the connection from $\bf x$ to $\bf t$ can be made assuming that the resulting vector $\bf t$ is the sum of a linear function $y:\mathbb{R}^M \to \mathbb{R}^k$ and a constant error term $\epsilon \sim \mathcal{N}(0, \beta^{-1})$ yielding

$$
	t = y({\bf x}, {\bf w}) + \varepsilon
$$

Under these assumptions, $t \sim \mathcal{N}\left(y({\bf x}, {\bf w}), \beta^{-1}\right)$, i.e., the target variable is a random variable governed by the observations and some weights $\bf w$

The choice of $y(x, w)$ will largely govern how complex our model can be.