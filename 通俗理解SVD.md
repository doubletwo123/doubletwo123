## SVD入门到实战

[TOC]

### 一、什么是特征向量与特征方程

+ <img src="通俗理解SVD.assets/image-20221027155547432.png" alt="image-20221027155547432" style="zoom:50%;" />

> 向量X1 、X2通过矩阵的映射变为AX1和AX2，如果通过映射的向量在方向（仍位于同一条直线上）上并未发生改变而是单单改变了向量的长度，这里称A为X2向量的特征方程，同时称lamda为X2的特征值，X2称为特征向量。
>
> <img src="通俗理解SVD.assets/image-20221027155913422.png" alt="image-20221027155913422" style="zoom: 67%;" />

+ 举个栗子：

  > <img src="通俗理解SVD.assets/image-20221027160154877.png" alt="image-20221027160154877" style="zoom:67%;" />

  ```java
  通过观察经翻转矩阵映射之后的图片可知，对于该翻转矩阵的特征向量为X1,对应的特征值为1
  而对于另一特征向量X2，对应的特征值为-1。
  ```


### 二、奇异值分解

+ [矩阵的【奇异值分解】(SVD)，图像压缩_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1B44y1C7CX/?spm_id_from=333.788.recommend_more_video.3&vd_source=16c13db1bc47b1b98f0b2e5bbe63cdbe)

+ 奇异值与特征显状挂钩，换句话说就是奇异值越大，奇异矩阵的秩越大，则越贴近于原图

  > ![image-20221027164958304](通俗理解SVD.assets/image-20221027164958304.png)
  >
  > <img src="通俗理解SVD.assets/image-20221027165048067.png" alt="image-20221027165048067" style="zoom:150%;" />

  > ![image-20221027164932503](通俗理解SVD.assets/image-20221027164932503.png)
  >
  > ![image-20221027165012500](通俗理解SVD.assets/image-20221027165012500.png)
  >
  > ![image-20221027165016902](通俗理解SVD.assets/image-20221027165016902.png)
  >
  > ![image-20221027165028279](通俗理解SVD.assets/image-20221027165028279.png)

+ 例如 rank=20表示的源图像，如下图

  > ![image-20221027165152214](通俗理解SVD.assets/image-20221027165152214.png)
  >
  > **当秩为1的时候最接近原图，由于秩为1矩阵行之间都是线性相关的，所以所有行只存在明暗程度的不同**
  >
  > 随着秩的增加，则则越接近原图，细节越清楚
  >
  > <img src="通俗理解SVD.assets/image-20221027165610408.png" alt="image-20221027165610408" style="zoom:67%;" />

+ ![image-20221027194237832](通俗理解SVD.assets/image-20221027194237832.png)