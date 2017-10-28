# Stanford-CS229-CN
斯坦福大学 CS229 讲义部分的翻译，想法来自于 **[这个仓库](https://github.com/Kivy-CN/Stanford-CS-229-CN)** 。
因为可能会对讲义内容有所修改补充，所以没有采用 Fork + PR 的形式，而是准备另起炉灶。然而，你看到的部分内容会和 [Kivy-CN](https://github.com/Kivy-CN) 等人贡献的内容类似。欢迎你维护上面提到的仓库中的翻译内容，他们已经获得了课程官方的授权。我们也欢迎所有人对此仓库进行维护和参与翻译优化工作。

查看 Markdown 格式文件时，你需要安装谷歌浏览器插件 [GitHub with MathJax](https://chrome.google.com/webstore/detail/ioemnmodlmafdkllaclgeombjnmnbima) 以正常显示数学公式，在对应小节整体翻译完成后我们会上传简单的PDF版本，也欢迎其他人提供优化过的PDF版本文件。有任何建议和错误都在 Issues 板块提出，Pull Requests 会在第一时间审核。详细的贡献方式请查看 [这篇文档](./CONTRIBUTING.md)。

> 本仓库仅供 MIL 交流学习使用，并不是官方授权的中文翻译，请勿公开传播使用

主要维护人员：曹骁威 （课程列表和翻译进度在本页面较下方处）  

## CS229 课程介绍

Stanford 课程主页地址：[http://cs229.stanford.edu/](http://cs229.stanford.edu/)
当前参考学期为：Autumn 2017

- 你可以[在这里](http://open.163.com/special/opencourse/machinelearning.html)访问一个古老版本的中文字幕课程视频，来自网易公开课。
- 你也可以在YOUTUBE上搜索CS229获得最新的视频内容

本课程将介绍机器学习和统计模式识别。主题包括：监督学习（判别算法/生成学习，参数/非参数学习，神经网络，支持向量机）; 无监督学习（聚类，降维，核方法）; 学习理论（偏差/方差权衡; VC理论;大间距）; 强化学习和自适应控制。课程还将讨论机器学习的近期应用，如机器人控制，数据挖掘，自主导航，生物信息学，语音识别，文本和网络数据处理。

### 先决条件

学生有以下背景：

- 掌握基本的计算机科学原理和技能，水平足以写出一个合理的微不足道的计算机程序。
- 熟悉[概率论](./English_Materials_and_Assignments/Section_Notes/cs229-prob.pdf)（CS 109或STATS 116）
- 熟悉[线性代数](./English_Materials_and_Assignments/Section_Notes/cs229-linalg.pdf)（Math 104，Math 113或CS 205中的任何一个应该是足够的）

**其它的介绍内容请访问课程主页。**

## 课程列表

**访问[这个链接](http://cs229.stanford.edu/syllabus.html)查看详细课程安排。**  

### 笔记一 \[[ps](./English_Materials_and_Assignments/Class_Notes/cs229-notes1.ps)\]\[[pdf](./English_Materials_and_Assignments/Class_Notes/cs229-notes1.pdf)\]\[[中文Markdown](./Translation/Notes/cs229-notes1-CN.md)\][中文PDF]

- Supervised learning
- Part I Linear Regression
  - 1 LMS algorithm
  - 2 The normal equations
    - 2.1 Matrix derivatives
    - 2.2 Least squares revisited
  - 3 Probabilistic interpretation
  - 4 Locally weighted linear regression
- Part II Classification and logistic regression
  - 5 Logistic regression
  - 6 Digression: The perceptron learning algorithm
  - 7 Another algorithm for maximizing ℓ(θ)
- Part III Generalized Linear Models
  - 8 The exponential family
  - 9 Constructing GLMs
    - 9.1 Ordinary Least Squares
    - 9.2 Logistic Regression
    - 9.3 Softmax Regression

### 笔记二 \[[ps](./English_Materials_and_Assignments/Class_Notes/cs229-notes2.ps)\]\[[pdf](./English_Materials_and_Assignments/Class_Notes/cs229-notes2.pdf)\]\[中文Markdown\][中文PDF]

- Part IV Generative Learning algorithms
  - 1 Gaussian discriminant analysis
    - 1.1 The multivariate normal distribution
    - 1.2 The Gaussian Discriminant Analysis model
    - 1.3 Discussion: GDA and logistic regression
  - 2 Naive Bayes
    - 2.1 Laplace smoothing
    - 2.2 Event models for text classification

### 笔记三 \[[ps](./English_Materials_and_Assignments/Class_Notes/cs229-notes3.ps)\]\[[pdf](./English_Materials_and_Assignments/Class_Notes/cs229-notes3.pdf)\]\[中文Markdown\][中文PDF]

- Part V Support Vector Machines
  - 1 Margins: Intuition
  - 2 Notation
  - 3 Functional and geometric margins
  - 4 The optimal margin classifier
  - 5 Lagrange duality
  - 6 Optimal margin classifiers
  - 7 Kernels
  - 8 Regularization and the non-separable case
  - 9 The SMO algorithm
    - 9.1 Coordinate ascent
    - 9.2 SMO

### 笔记四 \[[ps](./English_Materials_and_Assignments/Class_Notes/cs229-notes4.ps)\]\[[pdf](./English_Materials_and_Assignments/Class_Notes/cs229-notes4.pdf)\]\[中文Markdown\][中文PDF]

- Part VI Learning Theory
  - 1 Bias/variance tradeoff
  - 2 Preliminaries
  - 3 The case of finite $\cal H$
  - 4 The case of infinite $\cal H$

### 笔记五 \[[ps](./English_Materials_and_Assignments/Class_Notes/cs229-notes5.ps)\]\[[pdf](./English_Materials_and_Assignments/Class_Notes/cs229-notes5.pdf)\]\[中文Markdown\][中文PDF]

- Part VII Regularization and model selection
  - 1 Cross validation
  - 2 Feature Selection
  - 3 Bayesian statistics and regularization

### 笔记六 \[[ps](./English_Materials_and_Assignments/Class_Notes/cs229-notes6.ps)\]\[[pdf](./English_Materials_and_Assignments/Class_Notes/cs229-notes6.pdf)\]\[中文Markdown\][中文PDF]

- Online Learning and the Perceptron Algorithm. (optional reading) 
  - 1 The perceptron and large margin classiers

### 讨论凸优化（上） \[[ps](./English_Materials_and_Assignments/Section_Notes/cs229-cvxopt.ps)\]\[[pdf](./English_Materials_and_Assignments/Section_Notes/cs229-cvxopt.pdf)\]\[中文Markdown\][中文PDF]

- 1 Introduction
- 2 Convex Sets
  - 2.1 Examples
- 3 Convex Functions
  - 3.1 First Order Condition for Convexity
  - 3.2 Second Order Condition for Convexity
  - 3.3 Jensen’s Inequality
  - 3.4 Sublevel Sets
  - 3.5 Examples
- 4 Convex Optimization Problems
  - 4.1 Global Optimality in Convex Problems
  - 4.2 Special Cases of Convex Problems
  - 4.3 Examples
  - 4.4 Implementation: Linear SVM using CVX

### 讨论凸优化（下） \[[ps](./English_Materials_and_Assignments/Section_Notes/cs229-cvxopt2.ps)\]\[[pdf](./English_Materials_and_Assignments/Section_Notes/cs229-cvxopt2.pdf)\]\[中文Markdown\][中文PDF]

- 1 Lagrange duality
  - 1.1 The Lagrangian
  - 1.2 Primal and dual problems
  - 1.3 Interpreting the primal problem
  - 1.4 Interpreting the dual problem
  - 1.5 Complementary slackness
  - 1.6 The KKT conditions
- 2 A simple duality example
- 3 The $L_1$-norm soft margin SVM
- 4 Directions for further exploration

### 笔记七a \[[ps](./English_Materials_and_Assignments/Class_Notes/cs229-notes7a.ps)\]\[[pdf](./English_Materials_and_Assignments/Class_Notes/cs229-notes7a.pdf)\]\[中文Markdown\][中文PDF]

- The k-means clustering algorithm

### 笔记七b \[[ps](./English_Materials_and_Assignments/Class_Notes/cs229-notes7b.ps)\]\[[pdf](./English_Materials_and_Assignments/Class_Notes/cs229-notes7b.pdf)\]\[中文Markdown\][中文PDF]

- Mixtures of Gaussians and the EM algorithm

### 笔记八 \[[ps](./English_Materials_and_Assignments/Class_Notes/cs229-notes8.ps)\]\[[pdf](./English_Materials_and_Assignments/Class_Notes/cs229-notes8.pdf)\]\[中文Markdown\][中文PDF]

- Part IX The EM algorithm
  - 1 Jensen’s inequality
  - 2 The EM algorithm
  - 3 Mixture of Gaussians revisited

### 笔记九 \[[ps](./English_Materials_and_Assignments/Class_Notes/cs229-notes9.ps)\]\[[pdf](./English_Materials_and_Assignments/Class_Notes/cs229-notes9.pdf)]\[中文Markdown\][中文PDF]

- Part X Factor analysis
  - 1 Restrictions of $\sum$
  - 2 Marginals and conditionals of Gaussians
  - 3 The Factor analysis mode
  - 4 EM for factor analysis

### 笔记十 \[[ps](./English_Materials_and_Assignments/Class_Notes/cs229-notes10.ps)\]\[[pdf](./English_Materials_and_Assignments/Class_Notes/cs229-notes10.pdf)]\[中文Markdown\][中文PDF]

- Part XI Principal components analysis

### 笔记十一 \[[ps](./English_Materials_and_Assignments/Class_Notes/cs229-notes11.ps)\]\[[pdf](./English_Materials_and_Assignments/Class_Notes/cs229-notes11.pdf)]\[中文Markdown\][中文PDF]

- Part XII Independent Components Analysis

### 笔记十二 \[[ps](./English_Materials_and_Assignments/Class_Notes/cs229-notes12.ps)\]\[[pdf](./English_Materials_and_Assignments/Class_Notes/cs229-notes12.pdf)]\[中文Markdown\][中文PDF]

- Part XIII Reinforcement Learning and Control
  - 1 Markov decision processes
  - 2 Value iteration and policy iteration
  - 3 Learning a model for an MDP
  - 4 Continuous state MDPs
    - 4.1 Discretization
    - 4.2 Value function approximation
      - 4.2.1 Using a model or simulator
      - 4.2.2 Fitted value iteration

