---
title: Footnote Class
linktitle: Footnote
articleTitle: Footnote
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Notes.Footnote 类，这是您在文档中轻松、精确地管理脚注和尾注的重要工具。
type: docs
weight: 4950
url: /zh/net/aspose.words.notes/footnote/
---
## Footnote class

表示脚注或尾注文本的容器。

要了解更多信息，请访问[使用脚注和尾注](https://docs.aspose.com/words/net/working-with-footnote-and-endnote/)文档文章。

```csharp
public class Footnote : InlineStory
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [Footnote](footnote/)(*[DocumentBase](../../aspose.words/documentbase/), [FootnoteType](../footnotetype/)*) | 初始化`Footnote`类. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [ActualReferenceMark](../../aspose.words.notes/footnote/actualreferencemark/) { get; } | 获取此脚注在文档中显示的引用标记的实际文本。 |
| [Count](../../aspose.words/compositenode/count/) { get; } | 获取此节点的直属子节点的数量。 |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取此节点所属的文档。 |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | 获取节点的第一个子节点。 |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | 获取故事的第一段。 |
| [Font](../../aspose.words/inlinestory/font/) { get; } | 提供对此对象的锚字符的字体格式的访问。 |
| [FootnoteType](../../aspose.words.notes/footnote/footnotetype/) { get; } | 返回一个值，指定这是脚注还是尾注。 |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | 返回`真的`如果此节点有任何子节点。 |
| [IsAuto](../../aspose.words.notes/footnote/isauto/) { get; set; } | 保存一个值，该值指定这是一个自动编号的脚注还是带有用户定义的自定义引用标记的 脚注。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | 返回`真的`因为这个节点可以有子节点。 |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | 如果在启用更改跟踪的情况下在 Microsoft Word 中删除了此对象，则返回 true。 |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | 如果在启用更改跟踪的情况下将此对象插入 Microsoft Word，则返回 true。 |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | 返回`真的`如果在启用更改跟踪的情况下在 Microsoft Word 中移动（删除）此对象。 |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | 返回`真的`如果在启用更改跟踪的情况下在 Microsoft Word 中移动（插入）此对象。 |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | 获取节点的最后一个子节点。 |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | 获取故事的最后一段。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随此节点之后的节点。 |
| override [NodeType](../../aspose.words.notes/footnote/nodetype/) { get; } | 返回Footnote. |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | 获取故事的直接子段落集合。 |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | 检索父级[`Paragraph`](../../aspose.words/paragraph/)此节点的。 |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取此节点前一个节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回[`Range`](../../aspose.words/range/)表示此节点中包含的文档部分的对象。 |
| [ReferenceMark](../../aspose.words.notes/footnote/referencemark/) { get; set; } | 获取/设置用于此脚注的自定义引用标记。 默认值为**空字符串**(Empty)，表示使用自动编号的脚注。 |
| override [StoryType](../../aspose.words.notes/footnote/storytype/) { get; } | 返回Footnotes或者Endnotes. |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | 获取故事的直接子表集合。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words.notes/footnote/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | 接受访客。 |
| override [AcceptEnd](../../aspose.words.notes/footnote/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | 接受访客访问脚注末尾。 |
| override [AcceptStart](../../aspose.words.notes/footnote/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | 接受访客访问脚注的开头。 |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [Clone](../../aspose.words/node/clone/)(*bool*) | 创建节点的副本。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | 创建可用于遍历和读取节点的导航器。 |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | 如果最后一个子项不是段落，则创建并附加一个空段落。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | 获取指定的第一个祖先[`NodeType`](../../aspose.words/nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | 获取指定对象类型的第一个祖先。 |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | 返回与指定类型匹配的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | 为该节点的子节点提供对每个样式迭代的支持。 |
| override [GetText](../../aspose.words/compositenode/gettext/)() | 获取此节点及其所有子节点的文本。 |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | 返回子节点数组中指定子节点的索引。 |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | 在指定的参考节点后立即插入指定的节点。 |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | 在指定的参考节点之前立即插入指定的节点。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | 根据前序树遍历算法获取下一个节点。 |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | 将指定节点添加到此节点的子节点列表的开头。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | 根据前序树遍历算法获取前一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 将自身从父级中移除。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | 删除当前节点的所有子节点。 |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | 删除指定的子节点。 |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | 删除所有[`SmartTag`](../../aspose.words.markup/smarttag/)当前节点的后代节点。 |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | 选择与 XPath 表达式匹配的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | 选择第一个[`Node`](../../aspose.words/node/)与 XPath 表达式匹配。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的保存选项将节点内容导出为字符串。 |

## 评论

这`Footnote`类用于表示 Word 文档中的脚注和尾注。

`Footnote`是内联级节点，并且只能是[`Paragraph`](../../aspose.words/paragraph/)。

`Footnote`可以包含[`Paragraph`](../../aspose.words/paragraph/)和[`Table`](../../aspose.words.tables/table/)子节点。

## 例子

展示如何插入和自定义脚注。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 添加文本，并用脚注引用。此脚注将放置一个小的上标引用
// 在其引用的文本后进行标记，并在页面底部的正文下方创建一个条目。
// 此条目将包含脚注的引用标记和引用文本，
// 我们将把它传递给文档构建器的“InsertFootnote”方法。
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// 如果此属性设置为“true”，那么我们的脚注的引用标记
// 将成为该部分所有脚注中的索引。
// 这是第一个脚注，因此引用标记将为“1”。
Assert.True(footnote.IsAuto);

 // 我们可以将文档构建器移动到脚注内来编辑其参考文本。
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// 我们可以设置一个自定义引用标记，脚注将使用它来代替其索引号。
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// 将“IsAuto”标志设置为 true 的书签仍将显示其真实索引
// 即使以前的书签显示自定义引用标记，所以这个书签的引用标记将是“3”。
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### 也可以看看

* class [InlineStory](../../aspose.words/inlinestory/)
* 命名空间 [Aspose.Words.Notes](../../aspose.words.notes/)
* 部件 [Aspose.Words](../../)
