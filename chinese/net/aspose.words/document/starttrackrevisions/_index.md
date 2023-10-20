---
title: Document.StartTrackRevisions
linktitle: StartTrackRevisions
articleTitle: StartTrackRevisions
second_title: 用于 .NET 的 Aspose.Words
description: Document StartTrackRevisions 方法. 开始自动将您以编程方式对文档所做的所有进一步更改标记为修订更改 在 C#.
type: docs
weight: 710
url: /zh/net/aspose.words/document/starttrackrevisions/
---
## StartTrackRevisions(*string, DateTime*) {#starttrackrevisions_1}

开始自动将您以编程方式对文档所做的所有进一步更改标记为修订更改。

```csharp
public void StartTrackRevisions(string author, DateTime dateTime)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| author | String | 用于修订的作者姓名缩写。 |
| dateTime | DateTime | 用于修订的日期和时间。 |

## 评论

如果您调用此方法，然后以编程方式对文档进行一些更改， 保存文档并稍后在 MS Word 中打开文档，您将看到这些更改作为修订版本。

目前Aspose.Words仅支持跟踪节点插入和删除。格式更改不会 记录为修订版。

通过节点操作 修改本文档以及使用时都支持自动跟踪更改[`DocumentBuilder`](../../documentbuilder/)

此方法不会改变[`TrackRevisions`](../trackrevisions/)选项，并且不使用其 value 进行修订跟踪。

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

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## StartTrackRevisions(*string*) {#starttrackrevisions}

开始自动将您以编程方式对文档所做的所有进一步更改标记为修订更改。

```csharp
public void StartTrackRevisions(string author)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| author | String | 用于修订的作者姓名缩写。 |

## 评论

如果您调用此方法，然后以编程方式对文档进行一些更改， 保存文档并稍后在 MS Word 中打开文档，您将看到这些更改作为修订版本。

目前Aspose.Words仅支持跟踪节点插入和删除。格式更改不会 记录为修订版。

通过节点操作 修改本文档以及使用时都支持自动跟踪更改[`DocumentBuilder`](../../documentbuilder/)

此方法不会改变[`TrackRevisions`](../trackrevisions/)选项，并且不使用其 value 进行修订跟踪。

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

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
