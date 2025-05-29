---
title: Revision Class
linktitle: Revision
articleTitle: Revision
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Revision 类来管理文档中的修订追踪。轻松识别修订类型，实现无缝文档编辑。
type: docs
weight: 5500
url: /zh/net/aspose.words/revision/
---
## Revision class

表示文档节点或样式中的修订（跟踪更改）。 使用[`RevisionType`](./revisiontype/)检查此修订的类型。

要了解更多信息，请访问[跟踪文档中的修订](https://docs.aspose.com/words/net/track-changes-in-a-document/)文档文章。

```csharp
public class Revision
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Author](../../aspose.words/revision/author/) { get; set; } | 获取或设置此修订版的作者。不能为空字符串或`无效的`. |
| [DateTime](../../aspose.words/revision/datetime/) { get; set; } | 获取或设置此修订的日期/时间。 |
| [Group](../../aspose.words/revision/group/) { get; } | 获取修订组。返回`无效的`如果修订不属于任何组。 |
| [ParentNode](../../aspose.words/revision/parentnode/) { get; } | 获取此修订的直接父节点（所有者）。 此属性适用于除以下修订类型之外的任何修订类型StyleDefinitionChange. |
| [ParentStyle](../../aspose.words/revision/parentstyle/) { get; } | 获取此修订版的直接父样式（所有者）。 此属性仅适用于StyleDefinitionChange修订类型. |
| [RevisionType](../../aspose.words/revision/revisiontype/) { get; } | 获取此修订版的类型。 |

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
