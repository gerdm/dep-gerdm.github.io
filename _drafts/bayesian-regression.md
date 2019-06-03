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

The aim of this post is to motivate the bayesian framework for linear regression which, I believe, sheds a light on the frequentist view of linear regression

## Linear Regression and Basis Functions
A regression function is one that maps an $M$-dimensional input vector $\bf x$ to a $k$-dimensional output vector $\bf t$.

In its most simplest form, the connection from $\bf x$ to $\bf t$ can be made assuming that the resulting vector $\bf t$ is the sum of a linear function $y:\mathbb{R}^M \to \mathbb{R}^k$ and a constant error term $\epsilon \sim \mathcal{N}(0, \beta^{-1})$ yielding

$$
	t = y({\bf x}, {\bf w}) + \varepsilon
$$

Under these assumptions, $t \sim \mathcal{N}\left(y({\bf x}, {\bf w}), \beta^{-1}\right)$, i.e., the target variable is a random variable governed by the observations and some weights $\bf w$

The choice of $y(x, w)$ will largely govern how complex our model can be.
