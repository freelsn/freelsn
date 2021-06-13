---
title: 4.3 Composite (组合) -- 对象结构型模式
---

一般是树形结构。

Component 组件作为基类，Leaf 和 Composite 都继承 Component。Leaf 代表它只是一个组件。Composite 代表它是由多个组件构成的，其中的组件有可能是 Leaf 或者 Composite。

适用于“部分-整体”这种层次关系的结构。