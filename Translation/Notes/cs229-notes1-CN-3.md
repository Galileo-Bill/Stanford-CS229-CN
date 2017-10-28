原文：http://cs229.stanford.edu/notes/cs229-notes1.pdf  
翻译：[MIL Learning Group](https://github.com/milLearningGroup/Stanford-CS229-CN) - [San-greal](https://San-greal.github.io)

# Part III 广义线性模型(Generalized Linear Models)

到目前为止，我们已经看到了一个回归和一个分类的例子。在这个回归的例子中，我们有 $y|x$ $～$ $N$($\mu$,$\sigma^{2}$),而在这个分类的的例子中，有 $y|x$；$\theta$  $～$ 伯努利(Bernoulli)($\phi$)，对于 $\mu$ 和 $\phi$ 的一些适当的定义可以作为函数的 $x$ 和 $\theta$  。在这一节中，我们将展示这两种方法的更为广泛的家族模型的特殊情况，其称为广义线性模型（GLMS）。我们还将教授如何使用在GLM家族中的其他模型，并将他们应用于其他的分类与回归问题



## 8 The exponential family

​    为了进一步了解GLMS，我们先说一下指数分布，我们定义的一个分布如果是指数分布，则他可以被写为以下形式： 

​                                                                    $p(y;\eta) = b(y)exp(\eta^{T}T(y) - a(\eta))$                                                    $(6)$

该式子中的 $\eta$ 叫做**特性参数**(也叫做**典型参数**)；$T(y)$ 是**充分统计量**(通常情况下 $T(y) = y$)；而 $a(\eta)$ 是**对数划分函数**。分量 $e^{-a(\eta)}$ 的作用是归一化参数，确保 $p(y;\eta)$ 的和是大于1的。

​     $T$ 是一个复杂的选择，$a$ 和 $b$ 定义一个关于参数 $\eta$ 的分布族；当我们改变 $\eta$ 的值时，我们在这个分布族中能得到不同的分布。

​    现在看到的伯努利(Bernoulli)和高斯(Gaussian)分布都是指数分布的一个例子。伯努利(Bernoulli)分布均值为 $\phi$ 写为 Bernoulli( $\phi$ )，指定一个分布 $y \in {0,1}$ ，写成 $p (y = 1；\phi) = \phi ；p (y = 0；\phi) =1 - \phi$ 。

​    当我们改变 $\phi$ 的值，我们得到不同均值的伯努利(Bernoulli)分布。现在我们证明这一类的伯努利(Bernoulli)分布，在例子中选择 $T$ ，$a$ ，$b$ 所以式子(6)是伯努利(Bernoulli)分布。

我们把伯努利(Bernoulli)分布写为：

​	$p(y；\phi) = \phi^{y}(1 - \phi)^{1 - y}$ 

​	               $ = exp(ylog \phi + (1 - y)log(1 - \phi))$ 

​	               $ = exp((log\frac{\phi}{1 - \phi})y + log(1 - \phi))$ 

因此，特性参数由 $\eta = log(\phi/(1 - \phi))$ 给出。有意思的是，当我们使用 $\eta$ 表示 $\phi$ 的时候我们会得到 $\phi = 1/(1 + e^{-\eta})$ 。这看起来和S型(sigmoid)函数很像。当我们把逻辑回归分析看作GLM时这将会再次被提及。为了完成伯努利(Bernoulli)分布是指数分布的一种猜想，我们进一步得到：

​	$T(y) = y$ 

​         $a(\eta)  = -log(1 - \phi)$ 

​	          $ = log(1 + e^{\eta})$ 

​	 $ b(y) = 1$ 

这表明选择适当的 $T$ $a$ 和 $b$ 的时候，伯努利(Bernoulli)分布乐意被写为(6)的形式。我们进一步来讨论高斯(Gaussian)分布。回想一下，当我们推导线性回归时，$\sigma^{2}$ 的值对我们最终选择的 $\theta$ 和 $h_{\theta}(x)$ 没有任何影响。因此我们可以选择任意值作为 $\sigma^{2}$ 而不去改变他的值。为了简化式子，我们定义 $\sigma^2 = 1$ 。我们可以得到：

​	$p(y；\eta) = \frac{1}{\sqrt{2π}}exp(-\frac{1}{2}(y - \mu)^{2})$ 

​	               $ = \frac{1}{\sqrt{2π}}exp(-\frac{1}{2}y^{2})*exp(\mu y - \frac{1}{2}\mu^{2})$

因此，我们得出高斯(Gaussian)分布也在指数分布族里面，当

​	$ \eta = \mu$

  $T(y) = y$

  $a(\eta) = \mu^{2}/2$                                         

​	   $ = \eta^{2}/2$

   $b(y) = (1/\sqrt{2π})exp(-y^{2}/2)$ 

这有许多其他分布指数的成员：多项分布(我们稍后会遇见)，在泊松分布(造型计算数据；也看到问题集)；伽马和指数(造型连续，非负随机变量，如时间间隔)， $\beta$ 和狄利克雷(对概率分布)，以及更多。在下一节中，我们将描述构建模型的一般“食谱''，$y(x 和 \theta)$ 来自这些版本。     

## 9 Constructing GLMs



### 9.1 Ordinary Least Squares



### 9.2 Logistic Regression



### 9.3 Softmax Regression