---
title: Document.Clone
second_title: Aspose.Words for .NET API 参考
description: Document 方法. 执行深度复制Document.
type: docs
weight: 570
url: /zh/net/aspose.words/document/clone/
---
## Document.Clone method

执行深度复制[`Document`](../).

```csharp
public Document Clone()
```

### 返回值

克隆的文档。

### 例子

演示如何深度克隆文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

// 克隆将产生一个与原始内容相同的新文档，
// 但具有每个原始文档节点的唯一副本。
Document clone = doc.Clone();

Assert.AreEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetText(), 
    clone.FirstSection.Body.FirstParagraph.Runs[0].Text);
Assert.AreNotEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode(),
    clone.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode());
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)


