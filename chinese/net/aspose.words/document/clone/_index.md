---
title: Document.Clone
linktitle: Clone
articleTitle: Clone
second_title: 用于 .NET 的 Aspose.Words
description: Document Clone 方法. 对Document 在 C#.
type: docs
weight: 550
url: /zh/net/aspose.words/document/clone/
---
## Document.Clone method

对[`Document`](../).

```csharp
public Document Clone()
```

### 返回值

克隆的文档。

## 例子

演示如何深度克隆文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

// 克隆将产生一个与原始文件内容相同的新文档，
// 但是每个原始文档的节点都有一个唯一的副本。
Document clone = doc.Clone();

Assert.AreEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetText(), 
    clone.FirstSection.Body.FirstParagraph.Runs[0].Text);
Assert.AreNotEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode(),
    clone.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode());
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
