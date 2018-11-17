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
本次实验整体来说结果算是成功, 虽然其间不少有磕磕碰碰。 不得不说，sympy 是一个对新手及其友好的库，而且函数封装的很好，命名也很用心。
作为第一次接触符号运算的小白，在阅读 tutorial 的时候压力(除了英语单词)不算大。使用 sympy 库可以极其高效地完成如求积分，求导，级数展开，矩阵运算等等，而且还支持误差函数等，功能丰富，五脏俱全。相比之下，c 就...

<pre>
一些函数:
symbols   --->符号设置函数，当然也可以从 sympy.abc 引入一些符号
limit()   ---> 求极限
integrate()  --->求积分，不定积分，定积分均可
diff()          --->求导
matrix.det()  --->求行列式方法
matrix.inverse_GE()   --->高斯算法求逆矩阵方法
matrix.inverse_LU()   --->LU分解求逆矩阵方法
func.series()    --->泰勒展开式方法
pprint()         --->美观打印，其实并不怎么美观就是了

</pre>

<a href= "http://www.asmeurer.com/sympy_doc/dev-py3k/tutorial/tutorial.zh.html" > 
一个 sympy tutorial</a>


>人生苦短，我用 Python。

