---
title: Document.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words for .NET
description: 使用我们的文档克隆方法轻松复制您的文档。实现精准的深度复制，实现无缝编辑和高效的工作流程。
type: docs
weight: 590
url: /zh/net/aspose.words/document/clone/
---
## Document.Clone method

执行深层复制[`Document`](../).

```csharp
public Document Clone()
```

### 返回值

克隆的文档。

## 例子

展示如何深度克隆文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

// 克隆将产生一个与原始文档内容相同的新文档，
// 但具有原始文档的每个节点的唯一副本。
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
