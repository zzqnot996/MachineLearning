
## Wasserstein距离、最优传输和匈牙利匹配 概念解析

### Wasserstein距离：

Wasserstein距离是一种度量两个概率分布之间的差异或距离的方法。它的核心思想是考虑如何最有效地将一个分布的质量从一个位置移动到另一个位置，以使得两个分布尽可能地接近。这种移动的成本或代价通常表示为一个成本函数，它测量从一个位置到另一个位置的成本。

具体来说，Wasserstein距离通过求解最小成本的映射来计算，其中成本可以是欧氏距离、马氏距离或其他一些距离度量。这个距离度量考虑了分布之间的对应关系，即哪些部分的质量需要从一个位置移动到另一个位置。Wasserstein距离越小，表示两个分布越相似。

### 最优传输：

最优传输是一个更广泛的数学问题，它与Wasserstein距离密切相关。最优传输问题涉及将一种分布映射到另一种分布，以最小化某种成本或代价函数，同时满足一些约束条件。Wasserstein距离是最优传输问题的一个特例，其中成本函数通常是欧氏距离。

最优传输问题的一般形式如下：

给定两个概率分布 P 和 Q，以及一个成本函数 C(x, y)，其中 x 表示来自 P 的元素，y 表示来自 Q 的元素，目标是找到一个映射 T(x, y)，使得总成本最小化：

minimize∑x∑yC(x,y)⋅T(x,y)minimize∑x​∑y​C(x,y)⋅T(x,y)

同时满足一些约束条件，如保持分布的质量守恒等。

代表例子： Distribution Matching for Crowd Counting

### 匈牙利匹配：

匈牙利匹配是一个特定的组合优化问题，通常用于解决任务分配问题。在任务分配问题中，有一组任务和一组资源，每个任务需要分配到一个资源上，同时每个资源只能分配给一个任务。每个任务与资源之间都有一个成本或权重，目标是找到一种分配方式，以最小化总成本或总权重。

匈牙利匹配问题通常用于解决二分图中的最大匹配问题，其中任务和资源之间的关系可以表示为一个二分图。这个问题可以通过匈牙利算法高效地求解。

虽然这三个概念在某种程度上都涉及将一些东西从一个地方移到另一个地方以最小化某种成本或差异，但它们的应用领域和问题背景不同。Wasserstein距离主要用于度量概率分布之间的距离，最优传输是一个更一般化的数学问题，而匈牙利匹配用于解决任务分配和组合优化问题。它们各自具有不同的数学形式和应用背景。

代表例子： detr模型


## 学习资料

最优传输(Optimal Transport)问题与Wasserstein距离   ：  https://0809zheng.github.io/2022/05/16/Wasserstein.html

Source code for ot.bregman  ：  https://pythonot.github.io/_modules/ot/bregman.html#sinkhorn
