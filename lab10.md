# 实验报告: 用 Python 做计算器


<h2 align = "right">学号：18342106 </h2>
<h2 align = 'right'>姓名：谢正雄</h2>

## 实验目标：学会使用 sympy 库解决数学问题

## 步骤1. 用 Python 解决高数问题

`For example`，求极限

<a href="https://www.codecogs.com/eqnedit.php?latex=\lim_{x\to\pi/2}&space;(tan&space;x)^{2x-\pi}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\lim_{x\to\pi/2}&space;(tan&space;x)^{2x-\pi}" title="\lim_{x\to\pi/2} (tan x)^{2x-\pi}" /></a>

![](images/lim.png)

`再比如`，求不定积分

<a href="https://www.codecogs.com/eqnedit.php?latex=\int&space;\frac{sin(x)&plus;cos(x)}{2xin(x)-3cos(x)}dx" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\int&space;\frac{sin(x)&plus;cos(x)}{2xin(x)-3cos(x)}dx" title="\int \frac{sin(x)+cos(x)}{2xin(x)-3cos(x)}dx" /></a>

![](images/inte.png)

只要寥寥几行就能解决，这些困扰了我们许久的大问题

## 步骤2. 用 Python 解决线代问题

`For example` 求行列式

<a href="https://www.codecogs.com/eqnedit.php?latex=\begin{vmatrix}&space;5&space;&&space;6&space;&&space;8\\&space;3&&space;6&space;&&space;5\\&space;10&space;&&space;5&space;&&space;6&space;\end{vmatrix}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\begin{vmatrix}&space;5&space;&&space;6&space;&&space;8\\&space;3&&space;6&space;&&space;5\\&space;10&space;&&space;5&space;&&space;6&space;\end{vmatrix}" title="\begin{vmatrix} 5 & 6 & 8\\ 3& 6 & 5\\ 10 & 5 & 6 \end{vmatrix}" /></a>

![](images/det.png)

`再比如`求逆矩阵

![](images/inverse.png)

## 实验小结：
本次实验整体来说结果算是成功, 虽然其间不少有磕磕碰碰。 不得不说，sympy 是一个对新手及其友好的库，而且函数封装的很好，命名也很用心。使用 sympy 库可以极其高效地完成如求积分，求导，级数展开，矩阵运算等等，相比之下，c 就...

>人生苦短，我用 Python。

![一个 sympy tutorial](http://www.asmeurer.com/sympy_doc/dev-py3k/tutorial/tutorial.zh.html)