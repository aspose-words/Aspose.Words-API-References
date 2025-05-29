---
title: Node.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words for .NET
description: 使用节点克隆方法轻松复制节点。立即增强您的开发流程并简化项目效率！
type: docs
weight: 100
url: /zh/net/aspose.words/node/clone/
---
## Node.Clone method

创建节点的副本。

```csharp
public Node Clone(bool isCloneChildren)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| isCloneChildren | Boolean | 为 True 则递归克隆指定节点下的子树；为 false 则仅克隆节点本身。 |

### 返回值

克隆的节点。

## 评论

此方法用作节点的复制构造函数。 克隆的节点没有父节点，但与原始节点属于同一文档。

此方法始终执行节点的深度复制。*isCloneChildren* parameter 指定是否也执行复制所有子节点。

## 例子

展示如何克隆复合节点。

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;
para.AppendChild(new Run(doc, "Hello world!"));

// 以下是克隆复合节点的两种方法。
// 1 - 创建一个节点的克隆，并创建其每个子节点的克隆。
Node cloneWithChildren = para.Clone(true);

Assert.IsTrue(((CompositeNode)cloneWithChildren).HasChildNodes);
Assert.AreEqual("Hello world!", cloneWithChildren.GetText().Trim());

// 2 - 创建一个节点本身的克隆，没有任何子节点。
Node cloneWithoutChildren = para.Clone(false);

Assert.IsFalse(((CompositeNode)cloneWithoutChildren).HasChildNodes);
Assert.AreEqual(string.Empty, cloneWithoutChildren.GetText().Trim());
```

### 也可以看看

* class [Node](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
