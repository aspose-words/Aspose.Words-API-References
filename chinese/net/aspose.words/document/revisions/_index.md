---
title: Document.Revisions
linktitle: Revisions
articleTitle: Revisions
second_title: 用于 .NET 的 Aspose.Words
description: Document Revisions 财产. 获取此文档中存在的修订跟踪更改的集合 在 C#.
type: docs
weight: 350
url: /zh/net/aspose.words/document/revisions/
---
## Document.Revisions property

获取此文档中存在的修订（跟踪更改）的集合。

```csharp
public RevisionCollection Revisions { get; }
```

## 评论

返回的集合是一个“实时”集合，这意味着如果您删除包含 修订的文档部分，删除的修订将自动从该集合中消失。

## 例子

显示如何使用文档中的修订。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 文档的正常编辑不算作修订。
builder.Write("This does not count as a revision. ");

Assert.IsFalse(doc.HasRevisions);

// 要将我们的编辑注册为修订，我们需要声明作者，然后开始跟踪它们。
doc.StartTrackRevisions("John Doe", DateTime.Now);

builder.Write("This is revision #1. ");

Assert.IsTrue(doc.HasRevisions);
Assert.AreEqual(1, doc.Revisions.Count);

// 此标志对应于“评论”-> “跟踪”-> Microsoft Word 中的“跟踪更改”选项。
// “StartTrackRevisions”方法不影响它的值，
// 并且文档以编程方式跟踪修订，尽管它的值为“false”。
// 如果我们使用 Microsoft Word 打开此文档，它将不会跟踪修订。
Assert.IsFalse(doc.TrackRevisions);

// 我们使用文档构建器添加了文本，因此第一个修订版是插入类型的修订版。
Revision revision = doc.Revisions[0];
Assert.AreEqual("John Doe", revision.Author);
Assert.AreEqual("This is revision #1. ", revision.ParentNode.GetText());
Assert.AreEqual(RevisionType.Insertion, revision.RevisionType);
Assert.AreEqual(revision.DateTime.Date, DateTime.Now.Date);
Assert.AreEqual(doc.Revisions.Groups[0], revision.Group);

// 删除运行以创建删除类型的修订。
doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();

// 添加新的修订版将其放置在修订版集合的开头。
Assert.AreEqual(RevisionType.Deletion, doc.Revisions[0].RevisionType);
Assert.AreEqual(2, doc.Revisions.Count);

// 即使在我们接受/拒绝修订之前，插入修订也会显示在文档正文中。
// 拒绝修订将从正文中删除其节点。相反，构成删除修订的节点
// 也会在文档中逗留，直到我们接受修订。
Assert.AreEqual("This does not count as a revision. This is revision #1.", doc.GetText().Trim());

// 接受删除修订将从段落文本中删除其父节点
// 然后删除集合的修订本身。
doc.Revisions[0].Accept();

Assert.AreEqual(1, doc.Revisions.Count);
Assert.AreEqual("This is revision #1.", doc.GetText().Trim());

builder.Writeln("");
builder.Write("This is revision #2.");

// 现在移动节点以创建移动修订类型。
Node node = doc.FirstSection.Body.Paragraphs[1];
Node endNode = doc.FirstSection.Body.Paragraphs[1].NextSibling;
Node referenceNode = doc.FirstSection.Body.Paragraphs[0];

while (node != endNode)
{
    Node nextNode = node.NextSibling;
    doc.FirstSection.Body.InsertBefore(node, referenceNode);
    node = nextNode;
}

Assert.AreEqual(RevisionType.Moving, doc.Revisions[0].RevisionType);
Assert.AreEqual(8, doc.Revisions.Count);
Assert.AreEqual("This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc.GetText().Trim());

// 移动修订现在位于索引 1。拒绝修订以丢弃其内容。
doc.Revisions[1].Reject();

Assert.AreEqual(6, doc.Revisions.Count);
Assert.AreEqual("This is revision #1. \rThis is revision #2.", doc.GetText().Trim());
```

### 也可以看看

* class [RevisionCollection](../../revisioncollection/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
