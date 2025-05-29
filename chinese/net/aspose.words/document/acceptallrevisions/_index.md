---
title: Document.AcceptAllRevisions
linktitle: AcceptAllRevisions
articleTitle: AcceptAllRevisions
second_title: Aspose.Words for .NET
description: 使用 AcceptAllRevisions 方法简化您的编辑过程，轻松接受文档中所有跟踪的更改，以获得完善的最终版本。
type: docs
weight: 540
url: /zh/net/aspose.words/document/acceptallrevisions/
---
## Document.AcceptAllRevisions method

接受文档中的所有修订。

```csharp
public void AcceptAllRevisions()
```

## 评论

此方法是[`AcceptAll`](../../revisioncollection/acceptall/)。

## 例子

显示如何接受文档中的所有跟踪更改。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 在跟踪更改的同时编辑文档以创建一些修订。
doc.StartTrackRevisions("John Doe");
builder.Write("Hello world! ");
builder.Write("Hello again! ");
builder.Write("This is another revision.");
doc.StopTrackRevisions();

Assert.AreEqual(3, doc.Revisions.Count);

// 我们可以遍历每个修订版本并将其作为文档的一部分接受/拒绝。
// 如果我们知道我们希望接受每个修订，我们可以通过调用此方法更直接地做到这一点。
doc.AcceptAllRevisions();

Assert.AreEqual(0, doc.Revisions.Count);
Assert.AreEqual("Hello world! Hello again! This is another revision.", doc.GetText().Trim());
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
