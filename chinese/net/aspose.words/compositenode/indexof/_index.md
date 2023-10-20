---
title: CompositeNode.IndexOf
linktitle: IndexOf
articleTitle: IndexOf
second_title: 用于 .NET 的 Aspose.Words
description: CompositeNode IndexOf 方法. 返回子节点数组中指定子节点的索引 在 C#.
type: docs
weight: 120
url: /zh/net/aspose.words/compositenode/indexof/
---
## CompositeNode.IndexOf method

返回子节点数组中指定子节点的索引。

```csharp
public int IndexOf(Node child)
```

## 评论

如果在子节点中找不到该节点，则返回 -1。

## 例子

显示如何从其父节点获取给定子节点的索引。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

Body body = doc.FirstSection.Body;

// 检索第一节正文中最后一段的索引。
Assert.AreEqual(24, body.ChildNodes.IndexOf(body.LastParagraph));
```

### 也可以看看

* class [Node](../../node/)
* class [CompositeNode](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
