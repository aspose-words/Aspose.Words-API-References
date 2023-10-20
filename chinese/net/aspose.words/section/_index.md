---
title: Section Class
linktitle: Section
articleTitle: Section
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Section 班级. 表示文档中的单个部分 在 C#.
type: docs
weight: 5730
url: /zh/net/aspose.words/section/
---
## Section class

表示文档中的单个部分。

要了解更多信息，请访问[使用部分](https://docs.aspose.com/words/net/working-with-sections/)文档文章。

```csharp
public sealed class Section : CompositeNode
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [Section](section/)(*[DocumentBase](../documentbase/)*) | 初始化Section 类的新实例。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Body](../../aspose.words/section/body/) { get; } | 返回[`Body`](../body/)该节的子节点. |
| [Count](../../aspose.words/compositenode/count/) { get; } | 获取此节点的直接子节点的数量。 |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取该节点所属的文档。 |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | 获取节点的第一个子节点。 |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | 返回`真的`如果该节点有任何子节点. |
| [HeadersFooters](../../aspose.words/section/headersfooters/) { get; } | 提供对节的页眉和页脚节点的访问。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | 返回`真的`因为该节点可以有子节点。 |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | 获取节点的最后一个子节点。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随该节点的下一个节点。 |
| override [NodeType](../../aspose.words/section/nodetype/) { get; } | 返回Section. |
| [PageSetup](../../aspose.words/section/pagesetup/) { get; } | 返回一个表示页面设置和节属性的对象。 |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取紧邻此节点之前的节点。 |
| [ProtectedForForms](../../aspose.words/section/protectedforforms/) { get; set; } | 如果该部分受表单保护，则为真。当某个部分受到表单保护时， 用户只能选择和修改 Microsoft Word 中表单字段中的文本。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回一个[`Range`](../range/)表示此节点中包含的文档部分的对象。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words/section/accept/)(*[DocumentVisitor](../documentvisitor/)*) | 接受访客。 |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../node/)*) | 将指定节点添加到该节点的子节点列表的末尾。 |
| [AppendContent](../../aspose.words/section/appendcontent/)(*Section*) | 在本节末尾插入源节内容的副本。 |
| [ClearContent](../../aspose.words/section/clearcontent/)() | 清除该部分。 |
| [ClearHeadersFooters](../../aspose.words/section/clearheadersfooters/)() | 清除本节的页眉和页脚。 |
| [Clone](../../aspose.words/section/clone/#clone_1)() | 创建此部分的副本。 |
| [Clone](../../aspose.words/node/clone/)(*bool*) | 创建节点的副本。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | 创建可用于遍历和读取节点的导航器。 |
| [DeleteHeaderFooterShapes](../../aspose.words/section/deleteheaderfootershapes/)() | 删除本节页眉和页脚中的所有形状（绘图对象）。 |
| [EnsureMinimum](../../aspose.words/section/ensureminimum/)() | 确保该部分具有[`Body`](./body/)与一个[`Paragraph`](../paragraph/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | 获取指定的第一个祖先[`NodeType`](../nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | 获取指定对象类型的第一个祖先。 |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | 返回与指定类型匹配的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | 为该节点的子节点上的每个样式迭代提供支持。 |
| override [GetText](../../aspose.words/compositenode/gettext/)() | 获取此节点及其所有子节点的文本。 |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | 返回子节点数组中指定子节点的索引。 |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../node/), [Node](../node/)*) | 在指定的引用节点之后立即插入指定的节点。 |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../node/), [Node](../node/)*) | 在指定的引用节点之前插入指定的节点。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | 根据先序树遍历算法获取下一个节点。 |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../node/)*) | 将指定节点添加到该节点的子节点列表的开头。 |
| [PrependContent](../../aspose.words/section/prependcontent/)(*Section*) | 在本节的开头插入源节内容的副本。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | 根据先序树遍历算法获取前一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 将自身从父级中删除。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | 删除当前节点的所有子节点。 |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../node/)*) | 删除指定的子节点。 |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | 删除所有[`SmartTag`](../../aspose.words.markup/smarttag/)当前节点的后代节点. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | 选择与 XPath 表达式匹配的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | 选择第一个[`Node`](../node/)与 XPath 表达式匹配。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的保存选项将节点的内容导出到字符串中。 |

## 评论

`Section`可以拥有一个[`Body`](../body/)和最多一个[`HeaderFooter`](../headerfooter/)每个 [`HeaderFooterType`](../headerfootertype/) 。[`Body`](../body/)和[`HeaderFooter`](../headerfooter/) Nodes 内部可以是任意顺序`Section`。

最小有效部分需要具有[`Body`](../body/)与一个[`Paragraph`](../paragraph/)。

每个部分都有自己的一组属性，用于指定页面大小、方向、边距等。

您可以使用以下命令创建节的副本[`Clone`](../node/clone/)。该副本可以插入 相同或不同的文档中。

要添加、插入或删除整个节（包括分节符和 节属性），请使用以下方法[`Sections`](../document/sections/)目的。

要仅复制和插入节的内容（不包括分节符 和节属性），请使用[`AppendContent`](./appendcontent/)和[`PrependContent`](./prependcontent/)方法。

## 例子

展示如何手动构建 Aspose.Words 文档。

```csharp
Document doc = new Document();

// 一份空白文档包含一个部分、一个正文和一个段落。
// 调用“RemoveAllChildren”方法删除所有这些节点，
// 最终得到一个没有子节点的文档节点。
doc.RemoveAllChildren();

// 该文档现在没有可以添加内容的复合子节点。
// 如果我们希望编辑它，我们将需要重新填充它的节点集合。
// 首先，创建一个新节，然后将其作为子节点附加到根文档节点。
Section section = new Section(doc);
doc.AppendChild(section);

// 设置该部分的一些页面设置属性。
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// 一个部分需要一个主体，它将包含并显示其所有内容
// 在该部分的页眉和页脚之间的页面上。
Body body = new Body(doc);
section.AppendChild(body);

// 创建一个段落，设置一些格式属性，然后将其作为子项附加到正文。
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// 最后添加一些做文档的内容。创建一个运行，
// 设置其外观和内容，然后将其作为子项附加到段落中。
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### 也可以看看

* class [CompositeNode](../compositenode/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
