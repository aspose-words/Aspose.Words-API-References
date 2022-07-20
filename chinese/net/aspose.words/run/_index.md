---
title: Run
second_title: Aspose.Words for .NET API 参考
description: 表示一系列具有相同字体格式的字符
type: docs
weight: 4560
url: /zh/net/aspose.words/run/
---
## Run class

表示一系列具有相同字体格式的字符。

```csharp
public class Run : Inline
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [Run](run#constructor)(DocumentBase) | 初始化 **跑**类. |
| [Run](run#constructor_1)(DocumentBase, string) | 初始化 **跑**类. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | 指定自定义节点标识符。 |
| virtual [Document](../../aspose.words/node/document) { get; } | 获取该节点所属的文档。 |
| [Font](../../aspose.words/inline/font) { get; } | 提供对此对象的字体格式的访问。 |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | 如果此节点可以包含其他节点，则返回 true。 |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision) { get; } | 如果在启用更改跟踪时在 Microsoft Word 中删除了此对象，则返回 true。 |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision) { get; } | 如果启用更改跟踪时在 Microsoft Word 中更改了对象的格式，则返回 true。 |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision) { get; } | 如果在启用更改跟踪时将此对象插入 Microsoft Word，则返回 true。 |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision) { get; } | 返回 **真的**如果启用更改跟踪时此对象在 Microsoft Word 中被移动（删除）。 |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision) { get; } | 返回 **真的**如果启用更改跟踪时在 Microsoft Word 中移动（插入）此对象。 |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | 获取紧跟此节点的节点。 |
| override [NodeType](../../aspose.words/run/nodetype) { get; } | 返回 **节点类型运行**. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | 获取此节点的直接父节点。 |
| [ParentParagraph](../../aspose.words/inline/parentparagraph) { get; } | 检索父级[`Paragraph`](../paragraph)这个节点的. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | 获取紧接在此节点之前的节点。 |
| [Range](../../aspose.words/node/range) { get; } | 返回一个 **范围**表示此节点中包含的文档部分的对象。 |
| [Text](../../aspose.words/run/text) { get; set; } | 获取或设置运行的文本。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words/run/accept)(DocumentVisitor) | 接受访客。 |
| [Clone](../../aspose.words/node/clone)(bool) | 创建节点的副本。 |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | 获取指定的第一个祖先[`NodeType`](../nodetype). |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | 获取指定对象类型的第一个祖先。 |
| override [GetText](../../aspose.words/run/gettext)() | 获取运行的文本。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | 根据前序树遍历算法获取下一个节点。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | 根据前序树遍历算法获取上一个节点。 |
| [Remove](../../aspose.words/node/remove)() | 从父级中移除自身。 |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | 使用指定的保存选项将节点的内容导出为字符串。 |

### 评论

文档的所有文本都存储在文本运行中。

**跑**只能是 **段落**或内联 **结构化文档标签**.

### 例子

显示如何使用其字体属性格式化文本运行。

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

展示如何手动构建 Aspose.Words 文档。

```csharp
Document doc = new Document();

// 一个空白文档包含一个部分、一个正文和一个段落。
// 调用“RemoveAllChildren”方法来移除所有这些节点，
// 最后得到一个没有子节点的文档节点。
doc.RemoveAllChildren();

// 这个文档现在没有我们可以添加内容的复合子节点。
// 如果我们想编辑它，我们需要重新填充它的节点集合。
// 首先，创建一个新部分，然后将其作为子节点附加到根文档节点。
Section section = new Section(doc);
doc.AppendChild(section);

// 为该部分设置一些页面设置属性。
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// 一个section需要一个body，它将包含并显示它的所有内容
// 在节的页眉和页脚之间的页面上。
Body body = new Body(doc);
section.AppendChild(body);

// 创建一个段落，设置一些格式属性，然后将其作为子项附加到正文中。
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// 最后，添加一些内容来做文档。创建运行，
// 设置其外观和内容，然后将其作为子项附加到段落中。
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

展示如何在 CompositeNode 的子节点集合中添加、更新和删除子节点。

```csharp
Document doc = new Document();

// 默认情况下，一个空文档有一个段落。
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// 像我们的段落这样的复合节点可以包含其他复合和内联节点作为子节点。
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

//再创建三个运行节点。
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// 文档正文不会显示这些运行，直到我们将它们插入到复合节点中
// 它本身就是文档节点树的一部分，就像我们在第一次运行时所做的那样。
// 我们可以确定我们插入的节点的文本内容在哪里
// 通过指定相对于段落中另一个节点的插入位置出现在文档中。
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// 将第二次运行插入到第一次运行之前的段落中。
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// 在初始运行之后插入第三次运行。
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// 将第一次运行插入段落子节点集合的开头。
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// 我们可以通过编辑删除已有的子节点来修改run的内容。
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### 也可以看看

* class [Inline](../inline)
* 命名空间 [Aspose.Words](../../aspose.words)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
