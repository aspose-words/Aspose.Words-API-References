---
title: Document.StopTrackRevisions
linktitle: StopTrackRevisions
articleTitle: StopTrackRevisions
second_title: Aspose.Words for .NET
description: 了解如何使用 StopTrackRevisions 方法来防止自动文档更改标记，从而提高您的编辑效率和文档清晰度。
type: docs
weight: 770
url: /zh/net/aspose.words/document/stoptrackrevisions/
---
## Document.StopTrackRevisions method

停止自动将文档更改标记为修订。

```csharp
public void StopTrackRevisions()
```

## 例子

展示如何在编辑文档时跟踪修订。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 编辑文档通常不算作修订，直到我们开始跟踪它们。
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.IsTrue((DateTime.Now - doc.Revisions[0].DateTime).Milliseconds <= 10);

// 停止跟踪修订，以免将任何未来的编辑计为修订。
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// 创建修订版本会为其提供操作的日期和时间。
// 当我们开始跟踪修订时，我们可以通过传递 DateTime.MinValue 来禁用此功能。
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// 我们可以通过编程接受/拒绝这些修订
// 通过调用诸如 Document.AcceptAllRevisions 之类的方法，或者每个修订的 Accept 方法。
// 在 Microsoft Word 中，我们可以通过“审阅”->“更改”手动处理它们。
doc.Save(ArtifactsDir + "Revision.StartTrackRevisions.docx");
```

### 也可以看看

* method [StartTrackRevisions](../starttrackrevisions/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
