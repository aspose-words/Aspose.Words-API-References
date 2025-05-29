---
title: Inline Class
linktitle: Inline
articleTitle: Inline
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Inline 类，它专为内联节点中的字符格式化而设计。无需子节点即可增强文档的样式！
type: docs
weight: 3710
url: /zh/net/aspose.words/inline/
---
## Inline class

内联级节点的基类，可以具有与其关联的字符格式，但不能具有自己的子节点。

要了解更多信息，请访问[文档中节点的逻辑级别](https://docs.aspose.com/words/net/logical-levels-of-nodes-in-a-document/)文档文章。

```csharp
public abstract class Inline : Node
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取此节点所属的文档。 |
| [Font](../../aspose.words/inline/font/) { get; } | 提供对此对象的字体格式的访问。 |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | 返回`真的`如果此节点可以包含其他节点。 |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | 如果在启用更改跟踪的情况下在 Microsoft Word 中删除了此对象，则返回 true。 |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | 如果在启用更改跟踪的情况下 Microsoft Word 中的对象格式发生更改，则返回 true。 |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | 如果在启用更改跟踪的情况下将此对象插入 Microsoft Word，则返回 true。 |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | 返回`真的`如果在启用更改跟踪的情况下在 Microsoft Word 中移动（删除）此对象。 |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | 返回`真的`如果在启用更改跟踪的情况下在 Microsoft Word 中移动（插入）此对象。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随此节点之后的节点。 |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | 获取此节点的类型。 |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | 检索父级[`Paragraph`](../paragraph/)此节点的。 |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取此节点前一个节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回[`Range`](../range/)表示此节点中包含的文档部分的对象。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | 接受访客。 |
| [Clone](../../aspose.words/node/clone/)(*bool*) | 创建节点的副本。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | 获取指定的第一个祖先[`NodeType`](../nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | 获取指定对象类型的第一个祖先。 |
| virtual [GetText](../../aspose.words/node/gettext/)() | 获取此节点及其所有子节点的文本。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | 根据前序树遍历算法获取下一个节点。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | 根据前序树遍历算法获取前一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 将自身从父级中移除。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的保存选项将节点内容导出为字符串。 |

## 评论

派生自`Inline`可以是[`Paragraph`](../paragraph/)。

## 例子

展示如何确定内联节点的修订类型。

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// 当我们编辑文档时，可以通过“审阅”->“跟踪”找到“跟踪更改”选项，
// 在 Microsoft Word 中打开，我们应用的更改算作修订。
// 使用 Aspose.Words 编辑文档时，我们可以通过以下方式开始跟踪修订
// 调用文档的“StartTrackRevisions”方法并使用“StopTrackRevisions”方法停止跟踪。
// 我们可以接受修订并将其融入文档
// 或拒绝他们以有效地更改所提议的变更。
Assert.AreEqual(6, doc.Revisions.Count);

// 修订的父节点是该修订所涉及的运行。运行是一个内联节点。
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// 以下是五种可以标记内联节点的修订类型。
// 1 - “插入”修订：
// 当我们在跟踪更改时插入文本时会发生此修订。
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - “格式”修订：
// 当我们在跟踪更改的同时更改文本的格式时，就会发生此修订。
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - “移出”修订：
// 当我们在 Microsoft Word 中突出显示文本，然后将其拖动到文档中的其他位置时
// 跟踪更改时，出现两个修订版本。
// “移动自”修订版是我们移动它之前的原始文本的副本。
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 – “移至”修订：
// “移动到”修订版是我们将文本移动到文档中的新位置。
// 我们执行的每次移动修订中，“从...移动”和“移动到...修订”都会成对出现。
// 接受移动修订将删除“移动自”修订及其文本，
// 并保留“移至”修订版中的文本。
// 拒绝移动修订则相反地保留“移动自”修订并删除“移动到”修订。
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - “删除”修订：
// 当我们在跟踪更改时删除文本时，会发生此修订。当我们删除这样的文本时，
// 它将作为修订版本保留在文档中，直到我们接受该修订版本，
// 这将永久删除文本，或拒绝修订，这将保留我们删除的文本原位。
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### 也可以看看

* class [Node](../node/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
