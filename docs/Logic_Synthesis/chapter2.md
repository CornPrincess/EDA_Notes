## Notation

##  GRAPHS

## COMBINATORIAL OPTIMIZATION

Computer-aided design of microelectronic circuits requires modeling some design problems in a precise mathematical framework, which supports problem analysis and development of solution methods. Most architectural and logic design problems for digital circuits are discrete in nature. It is therefore necessary to solve **combinatorial  decision** and **optimization problems**.

微电子电路的计算机辅助设计需要在精确的数学框架中对一些设计问题进行建模，从而支持问题分析和解决方法的开发。 **数字电路的大多数架构和逻辑设计问题本质上都是离散的。 因此有必要解决组合决策和优化问题。**

A decision problem is a problem with a binary-valued solution: TRUE or FALSE. Such problems are related to testing some properties of a model, for example, questioning the existence of a vertex coloring with k colors in a given graph. 

决策问题是具有二进制值解决方案的问题：TRUE 或 FALSE。此类问题与测试模型的某些属性有关，例如，质疑给定图中是否存在具有 k 种颜色的顶点着色。

An optimization problem is a problem whose solution can be measured in terms of a cost (or objective) function and such that the cost function attains a maximum or minimum value. For example, the search for a vertex coloring with a minimum number of colors in a given graph is an optimization problem. 

优化问题是一个问题，其解决方案可以根据成本（或目标）函数来衡量，并且成本函数达到最大值或最小值。例如，在给定图形中搜索具有最少颜色数量的顶点着色是一个优化问题。 

Optimization problems can be reduced to sequences of decision problems and are always at least as difficult to solve as the corresponding decision problems. For this reason, in problem complexity analysis, only decision problems are considered, because they provide a lower bound on the complexity of the corresponding optimization problem. Nevertheless, solution methods to optimization problems do not necessarily need to solve sequences of decision problems. 

优化问题可以简化为一系列决策问题，并且总是至少与相应的决策问题一样难以解决。因此，在问题复杂性分析中，只考虑决策问题， 因为它们提供了相应优化问题复杂度的下限。然而，优化问题的解决方法不一定需要解决决策问题的序列。

## Tractable and Intractable Problems 

[浅谈P、NP、NP-Complate和NP-Hard问题 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/433308577)