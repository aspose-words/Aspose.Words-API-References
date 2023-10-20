---
title: Inline Class
linktitle: Inline
articleTitle: Inline
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Inline 班级. 内联级节点的基类可以具有与其关联的字符格式但不能拥有自己的子节点 在 C#.
type: docs
weight: 3260
url: /zh/net/aspose.words/inline/
---
## Inline class

内联级节点的基类，可以具有与其关联的字符格式，但不能拥有自己的子节点。

要了解更多信息，请访问[文档中节点的逻辑级别](https://docs.aspose.com/words/net/logical-levels-of-nodes-in-a-document/)文档文章。

```csharp
public abstract class Inline : Node
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取该节点所属的文档。 |
| [Font](../../aspose.words/inline/font/) { get; } | 提供对此对象的字体格式的访问。 |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | 返回`真的`如果该节点可以包含其他节点. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | 如果在启用更改跟踪时在 Microsoft Word 中删除了此对象，则返回 true。 |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | 如果在启用更改跟踪的情况下在 Microsoft Word 中更改了对象的格式，则返回 true。 |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | 如果在启用更改跟踪的情况下将此对象插入到 Microsoft Word 中，则返回 true。 |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | 返回`真的`如果启用更改跟踪时在 Microsoft Word 中移动（删除）此对象。 |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | 返回`真的`如果在启用更改跟踪的情况下在 Microsoft Word 中移动（插入）此对象。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随该节点的下一个节点。 |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | 获取此节点的类型。 |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | 检索父级[`Paragraph`](../paragraph/)此节点的. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取紧邻此节点之前的节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回一个[`Range`](../range/)表示此节点中包含的文档部分的对象。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | 接受访客。 |
| [Clone](../../aspose.words/node/clone/)(*bool*) | 创建节点的副本。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | 获取指定的第一个祖先[`NodeType`](../nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | 获取指定对象类型的第一个祖先。 |
| virtual [GetText](../../aspose.words/node/gettext/)() | 获取此节点及其所有子节点的文本。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | 根据先序树遍历算法获取下一个节点。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | 根据先序树遍历算法获取前一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 将自身从父级中删除。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的保存选项将节点的内容导出到字符串中。 |

## 评论

一个类派生自`Inline`可以是以下的孩子[`Paragraph`](../paragraph/)。

## 例子

演示如何确定内联节点的修订类型。

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// 当我们编辑文档的时候有“Track Changes”选项，在via Review中找到->追踪，
// 在 Microsoft Word 中打开，我们应用的更改算作修订。
// 使用 Aspose.Words 编辑文档时，我们可以通过以下方式开始跟踪修订
// 调用文档的“StartTrackRevisions”方法并使用“StopTrackRevisions”方法停止跟踪。
// 我们可以接受修订以将它们吸收到文档中
// 或拒绝他们以有效地更改提议的更改。
Assert.AreEqual(6, doc.Revisions.Count);

// 修订版的父节点是该修订版涉及的运行。 Run 是一个内联节点。
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// 以下是可以标记内联节点的五种类型的修订。
// 1 - “插入”修订：
// 当我们在跟踪更改时插入文本时，会发生此修订。
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - “格式”修订：
// 当我们在跟踪更改的同时更改文本格式时，就会发生此修订。
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - “移自”修订版：
// 当我们在 Microsoft Word 中突出显示文本，然后将其拖动到文档中的其他位置时
// 跟踪更改时，会出现两个修订。
// “移自”修订版是我们移动文本之前的原始文本的副本。
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - “移动到”修订版：
// “移动到”修订版是我们移动到文档中新位置的文本。
// 对于我们执行的每个移动修订，“移动自”和“移动至”修订成对出现。
// 接受移动修订会删除“移动自”修订及其文本，
// 并保留“移至”修订版中的文本。
// 相反，拒绝移动修订会保留“移自”修订并删除“移至”修订。
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - “删除”修订版：
// 当我们在跟踪更改的同时删除文本时，会发生此修订。当我们删除这样的文本时，
// 它将作为修订版保留在文档中，直到我们接受修订版，
// 这将永久删除文本，或者拒绝修订，这将使我们删除的文本保留在原来的位置。
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### 也可以看看

* class [Node](../node/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
