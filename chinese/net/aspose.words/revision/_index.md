---
title: Revision Class
linktitle: Revision
articleTitle: Revision
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Revision 班级. 表示文档节点或样式中的修订跟踪更改 使用RevisionType检查此修订的类型 在 C#.
type: docs
weight: 4760
url: /zh/net/aspose.words/revision/
---
## Revision class

表示文档节点或样式中的修订（跟踪更改）。 使用[`RevisionType`](./revisiontype/)检查此修订的类型。

要了解更多信息，请访问[跟踪文档中的更改](https://docs.aspose.com/words/net/track-changes-in-a-document/)文档文章。

```csharp
public class Revision
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Author](../../aspose.words/revision/author/) { get; set; } | 获取或设置此修订版的作者。不能为空字符串或`无效的`. |
| [DateTime](../../aspose.words/revision/datetime/) { get; set; } | 获取或设置此修订的日期/时间。 |
| [Group](../../aspose.words/revision/group/) { get; } | 获取修订组。退货`无效的`如果修订版不属于任何组。 |
| [ParentNode](../../aspose.words/revision/parentnode/) { get; } | 获取此修订版的直接父节点（所有者）。 此属性适用于除StyleDefinitionChange. |
| [ParentStyle](../../aspose.words/revision/parentstyle/) { get; } | 获取此修订版的直接父样式（所有者）。 此属性仅适用于StyleDefinitionChange修订类型. |
| [RevisionType](../../aspose.words/revision/revisiontype/) { get; } | 获取此修订版本的类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Accept](../../aspose.words/revision/accept/)() | 接受此修订。 |
| [Reject](../../aspose.words/revision/reject/)() | 拒绝此修订。 |

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
