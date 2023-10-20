---
title: Revision.Reject
linktitle: Reject
articleTitle: Reject
second_title: 用于 .NET 的 Aspose.Words
description: Revision Reject 方法. 拒绝此修订 在 C#.
type: docs
weight: 80
url: /zh/net/aspose.words/revision/reject/
---
## Revision.Reject method

拒绝此修订。

```csharp
public void Reject()
```

## 例子

展示如何处理文档中的修订。

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

// 该标志对应于“Review”-> 「追踪」-> Microsoft Word 中的“跟踪更改”选项。
// “StartTrackRevisions”方法不影响其值，
// 并且该文档正在以编程方式跟踪修订，尽管它的值为“false”。
// 如果我们使用 Microsoft Word 打开此文档，它将不会跟踪修订。
Assert.IsFalse(doc.TrackRevisions);

// 我们使用文档生成器添加了文本，因此第一个修订版是插入型修订版。
Revision revision = doc.Revisions[0];
Assert.AreEqual("John Doe", revision.Author);
Assert.AreEqual("This is revision #1. ", revision.ParentNode.GetText());
Assert.AreEqual(RevisionType.Insertion, revision.RevisionType);
Assert.AreEqual(revision.DateTime.Date, DateTime.Now.Date);
Assert.AreEqual(doc.Revisions.Groups[0], revision.Group);

// 删除运行以创建删除类型修订。
doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();

// 添加新修订将其放置在修订集合的开头。
Assert.AreEqual(RevisionType.Deletion, doc.Revisions[0].RevisionType);
Assert.AreEqual(2, doc.Revisions.Count);

// 在我们接受/拒绝修订之前插入显示在文档正文中的修订。
// 拒绝修订将从正文中删除其节点。相反，组成删除修订的节点
// 也停留在文档中，直到我们接受修订。
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

* class [Revision](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
