---
title: Document.StopTrackRevisions
linktitle: StopTrackRevisions
articleTitle: StopTrackRevisions
second_title: 用于 .NET 的 Aspose.Words
description: Document StopTrackRevisions 方法. 停止将文档更改自动标记为修订版 在 C#.
type: docs
weight: 720
url: /zh/net/aspose.words/document/stoptrackrevisions/
---
## Document.StopTrackRevisions method

停止将文档更改自动标记为修订版。

```csharp
public void StopTrackRevisions()
```

## 例子

展示如何在编辑文档时跟踪修订。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 在我们开始跟踪文档之前，编辑文档通常不算作修订。
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.That(doc.Revisions[0].DateTime, Is.EqualTo(DateTime.Now).Within(10).Milliseconds);

// 停止跟踪修订，以不将任何未来的编辑算作修订。
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// 创建修订为它们提供操作的日期和时间。
// 当我们开始跟踪修订时，我们可以通过传递 DateTime.MinValue 来禁用此功能。
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// 我们可以以编程方式接受/拒绝这些修订
// 通过调用 Document.AcceptAllRevisions 等方法或每个修订版的 Accept 方法。
// 在 Microsoft Word 中，我们可以通过“审阅”-> 手动处理它们“变化”。
doc.Save(ArtifactsDir + "Document.StartTrackRevisions.docx");
```

### 也可以看看

* method [StartTrackRevisions](../starttrackrevisions/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
