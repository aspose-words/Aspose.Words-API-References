---
title: Revision.Author
linktitle: Author
articleTitle: Author
second_title: Aspose.Words for .NET
description: 轻松管理修订作者。轻松设置或更新每次修订的作者详细信息，确保文档清晰易懂、责任明确。
type: docs
weight: 10
url: /zh/net/aspose.words/revision/author/
---
## Revision.Author property

获取或设置此修订版的作者。不能为空字符串或`无效的`.

```csharp
public string Author { get; set; }
```

## 例子

展示如何处理文档中的修订。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 对文档的正常编辑不算作修订。
builder.Write("This does not count as a revision. ");

Assert.IsFalse(doc.HasRevisions);

// 要将我们的编辑注册为修订，我们需要声明一个作者，然后开始跟踪它们。
doc.StartTrackRevisions("John Doe", DateTime.Now);

builder.Write("This is revision #1. ");

Assert.IsTrue(doc.HasRevisions);
Assert.AreEqual(1, doc.Revisions.Count);

// 此标志对应于 Microsoft Word 中的“审阅”->“跟踪”->“跟踪更改”选项。
//“StartTrackRevisions”方法不会影响其值，
// 尽管值为“false”，但文档仍以编程方式跟踪修订。
// 如果我们使用 Microsoft Word 打开此文档，它将不会跟踪修订。
Assert.IsFalse(doc.TrackRevisions);

// 我们已经使用文档构建器添加了文本，因此第一次修订是插入类型的修订。
Revision revision = doc.Revisions[0];
Assert.AreEqual("John Doe", revision.Author);
Assert.AreEqual("This is revision #1. ", revision.ParentNode.GetText());
Assert.AreEqual(RevisionType.Insertion, revision.RevisionType);
Assert.AreEqual(revision.DateTime.Date, DateTime.Now.Date);
Assert.AreEqual(doc.Revisions.Groups[0], revision.Group);

// 删除运行以创建删除类型修订。
doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();

// 添加新的修订版本会将其放置在修订版本集合的开头。
Assert.AreEqual(RevisionType.Deletion, doc.Revisions[0].RevisionType);
Assert.AreEqual(2, doc.Revisions.Count);

// 在我们接受/拒绝修订之前，插入修订就会显示在文档正文中。
// 拒绝修订版本将从主体中删除其节点。相反，组成修订版本的节点将被删除
// 也停留在文档中直到我们接受修订。
Assert.AreEqual("This does not count as a revision. This is revision #1.", doc.GetText().Trim());

// 接受删除修订将从段落文本中删除其父节点
// 然后删除集合本身的修订版本。
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
