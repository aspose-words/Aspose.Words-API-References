---
title: Section
second_title: Aspose.Words for .NET API 参考
description: 表示文档中的单个部分
type: docs
weight: 5390
url: /zh/net/aspose.words/section/
---
## Section class

表示文档中的单个部分。

```csharp
public sealed class Section : CompositeNode
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [Section](section)(DocumentBase) | 初始化 Section 类的新实例。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Body](../../aspose.words/section/body) { get; } | 返回该节的 **Body** 子节点。 |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | 获取该节点的所有直接子节点。 |
| [Count](../../aspose.words/compositenode/count) { get; } | 获取此节点的直接子节点数。 |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | 指定自定义节点标识符。 |
| virtual [Document](../../aspose.words/node/document) { get; } | 获取该节点所属的文档。 |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | 获取节点的第一个子节点。 |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | 如果此节点有任何子节点，则返回 true。 |
| [HeadersFooters](../../aspose.words/section/headersfooters) { get; } | 提供对节的页眉和页脚节点的访问。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | 返回真，因为该节点可以有子节点。 |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | 获取节点的最后一个子节点。 |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | 获取紧跟该节点的节点。 |
| override [NodeType](../../aspose.words/section/nodetype) { get; } | 返回 **NodeType.Section** 。 |
| [PageSetup](../../aspose.words/section/pagesetup) { get; } | 返回一个表示页面设置和部分属性的对象。 |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | 获取此节点的直接父节点。 |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | 获取紧接在此节点之前的节点。 |
| [ProtectedForForms](../../aspose.words/section/protectedforforms) { get; set; } | 如果该部分受到表单保护，则为真。当某个部分受表单保护时， 用户只能在 Microsoft Word 的表单域中选择和修改文本。 |
| [Range](../../aspose.words/node/range) { get; } | 返回 **Range** 对象，该对象表示包含在此节点中的文档部分。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words/section/accept)(DocumentVisitor) | 接受访问者。 |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [AppendContent](../../aspose.words/section/appendcontent)(Section) | 在本节末尾插入源节内容的副本。 |
| [ClearContent](../../aspose.words/section/clearcontent)() | 清除该部分。 |
| [ClearHeadersFooters](../../aspose.words/section/clearheadersfooters)() | 清除本节的页眉和页脚。 |
| [Clone](../../aspose.words/section/clone#clone_1)() | 创建此部分的副本。 |
| [Clone](../../aspose.words/node/clone)(bool) | 创建节点的副本。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | 保留供系统使用。 IXPath 可导航。 |
| [DeleteHeaderFooterShapes](../../aspose.words/section/deleteheaderfootershapes)() | 从本节的页眉和页脚中删除所有形状（绘图对象）。 |
| [EnsureMinimum](../../aspose.words/section/ensureminimum)() | 确保该部分具有带有一个段落的正文。 |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | 获取指定[`NodeType`](../nodetype)的第一个祖先。 |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | 获取指定对象类型的第一个祖先。 |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | 返回匹配指定类型的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | 为在此节点的子节点上的每个样式迭代提供支持。 |
| override [GetText](../../aspose.words/compositenode/gettext)() | 获取该节点及其所有子节点的文本。 |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | 返回子节点数组中指定子节点的索引。 |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | 在指定参考节点之后立即插入指定节点。 |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | 在指定参考节点之前插入指定节点。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | 根据前序树遍历算法获取下一个节点。 |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | 将指定节点添加到该节点的子节点列表的开头。 |
| [PrependContent](../../aspose.words/section/prependcontent)(Section) | 在本节开头插入源节内容的副本。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | 根据前序树遍历算法获取上一个节点。 |
| [Remove](../../aspose.words/node/remove)() | 从父级中移除自身。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | 移除当前节点的所有子节点。 |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | 移除指定的子节点。 |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | 删除当前节点的所有[`SmartTag`](../../aspose.words.markup/smarttag)后代节点。 |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | 选择与 XPath 表达式匹配的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | 选择与 XPath 表达式匹配的第一个节点。 |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | 使用指定的保存选项将节点的内容导出为字符串。 |

### 评论

**Section** 可以有一个[`Body`](./body)和每个中最多一个R5:T:Aspose.Words.HeaderFooter::: T:Aspose.Words.HeaderFooterType:::。 **Body** 和 **HeaderFooter** 节点 可以在内部以任何顺序排列 **部分** 。

最小有效部分需要有 **正文** 和一个 **段落** 。

每个部分都有自己的一组属性，用于指定页面大小、方向、边距等。

您可以使用[`Clone`](../node/clone)创建部分的副本。副本可以插入到 相同或不同的文档中。

要添加、插入或删除整个节，包括分节符和 节属性，请使用 **的方法部分** 对象。

要复制和插入节的内容，不包括分节符 和节属性使用 **AppendContent** 和 **PrependContent** 方法。

### 例子

展示如何手动构建 Aspose.Words 文档。

```csharp
Document doc = new Document();

 // 一个空白文档包含一个部分、一个正文和一个段落。
 // 调用“RemoveAllChildren”方法删除所有节点，
 // 最终得到一个没有子节点的文档节点。
doc.RemoveAllChildren();

 // 这个文档现在没有我们可以添加内容的复合子节点。
// 如果我们想编辑它，我们需要重新填充它的节点集合。
 // 首先，创建一个新节，然后将其作为子节点附加到根文档节点。
Section section = new Section(doc);
doc.AppendChild(section);

 // 为部分设置一些页面设置属性。
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

 // 一个部分需要一个主体，它将包含并显示其所有内容
 // 在节的页眉和页脚之间的页面上。
Body body = new Body(doc);
section.AppendChild(body);

 // 创建一个段落，设置一些格式属性，然后将其作为子项附加到 body.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

 // 最后，添加一些内容来做文档。创建一个运行，
 // 设置其外观和内容，然后将其作为子项附加到段落中。
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### 也可以看看

* class [CompositeNode](../compositenode)
* 命名空间 [Aspose.Words](../../aspose.words)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
