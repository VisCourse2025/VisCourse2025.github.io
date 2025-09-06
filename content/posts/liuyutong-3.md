---
title: 优秀案例-实验3降维可视化-刘与同
summary: 鸢尾花数据集经PCA、MDS与t-SNE降维对比，结果显示t-SNE分离效果最佳，类别区分更直观明显。
image: images/liuyutong-3.png
date: "2025-09-06"
tags:
  - 降维可视化
---
鸢尾花数据集可通过 sklearn 库加载，数据集的特征和标签如下：

- 特征：萼片长度，萼片宽度，花瓣长度，花瓣宽度
- 标签：，Iris-setosa，Iris-versicolor，Iris-virginica

降维时，我们使用三种降维方法对鸢尾花数据集进行降维：

- PCA: 一种线性降维方法，通过找到数据中的主成分来减少维度。通过最大化降维之后的方差，最大程度上保留原有数据的特征。
- MDS: 旨在保留样本之间的相对距离,适用于处理相似度或距离矩阵的数据。
- t-SNE: 一种非线性降维技术，特别关注样本之间的局部结构,也就是注重与原来那些较为临近的数据。

首先，调入 sklearn 加载鸢尾花数据集，并将数据分为特征和标签。使用PCA、MDS 和 t-SNE 对鸢尾花数据集进行降维，降至 2 维和 3 维。最后，调用 plotly 和 matplotlib 对降维结果进行可视化。

PCA 图显示了三种鸢尾花的类别在前两（三）个主成分上的分布。尽管 Iris-setosa 显示出明显的分离，但 Iris-versicolor 和 Iris-virginica 之间存在一定的重叠。

MDS 图保留了样本间的相对距离。与 PCA 相比，MDS 更加关注样本之间的相似性。

t-SNE 图展示了更明显的类别分离，尤其是 Iris-setosa 与其他两类之间的显著差异，因为t-SNE 能够更好地捕捉到数据中的复杂结构。将其与PCA对比，我们可以发现，t-SNE在降维之后，相同类型的鸢尾花的数据点更加靠近，分类更直观，说明特征选取的区分性更强。

对比三种图我们不难发现，在这种数据集中，t-SNE的效果最佳。

[liuyutong-iris_mds_visualization.html](/excellent_works/liuyutong-iris_mds_visualization.html)

[liuyutong-iris_pca_2d_visualization.html](/excellent_works/liuyutong-iris_pca_2d_visualization.html)

[liuyutong-iris_pca_visualization.html](/excellent_works/liuyutong-iris_pca_visualization.html)

[liuyutong-iris_tsne_2d_visualization.html](/excellent_works/liuyutong-iris_tsne_2d_visualization.html)

[liuyutong-iris_tsne_visualization.html](/excellent_works/liuyutong-iris_tsne_visualization.html)