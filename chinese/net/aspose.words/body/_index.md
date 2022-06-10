---
title: Body
second_title: Aspose.Words for .NET API 参考
description: 表示一个部分的主要文本的容器
type: docs
weight: 20
url: /zh/net/aspose.words/body/
---
## Body class

表示一个部分的主要文本的容器。

```csharp
public class Body : Story
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [Body](body)(DocumentBase) | 初始化 **Body** 类的新实例。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | 获取该节点的所有直接子节点。 |
| [Count](../../aspose.words/compositenode/count) { get; } | 获取此节点的直接子节点数。 |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | 指定自定义节点标识符。 |
| virtual [Document](../../aspose.words/node/document) { get; } | 获取该节点所属的文档。 |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | 获取节点的第一个子节点。 |
| [FirstParagraph](../../aspose.words/story/firstparagraph) { get; } | 获取故事的第一段。 |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | 如果此节点有任何子节点，则返回 true。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | 返回真，因为该节点可以有子节点。 |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | 获取节点的最后一个子节点。 |
| [LastParagraph](../../aspose.words/story/lastparagraph) { get; } | 获取故事的最后一段。 |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | 获取紧跟该节点的节点。 |
| override [NodeType](../../aspose.words/body/nodetype) { get; } | 返回 **NodeType.Body** 。 |
| [Paragraphs](../../aspose.words/story/paragraphs) { get; } | 获取作为故事直接子级的段落的集合。 |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | 获取此节点的直接父节点。 |
| [ParentSection](../../aspose.words/body/parentsection) { get; } | 获取此故事的父部分。 |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | 获取紧接在此节点之前的节点。 |
| [Range](../../aspose.words/node/range) { get; } | 返回 **Range** 对象，该对象表示包含在此节点中的文档部分。 |
| [StoryType](../../aspose.words/story/storytype) { get; } | 获取这个故事的类型。 |
| [Tables](../../aspose.words/story/tables) { get; } | 获取作为故事的直接子级的表的集合。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words/body/accept)(DocumentVisitor) | 接受访问者。 |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [AppendParagraph](../../aspose.words/story/appendparagraph)(string) | 创建带有可选文本的[`Paragraph`](../paragraph)对象并将其附加到该对象末尾的快捷方法。 |
| [Clone](../../aspose.words/node/clone)(bool) | 创建节点的副本。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | 保留供系统使用。 IXPath 可导航。 |
| [DeleteShapes](../../aspose.words/story/deleteshapes)() | 从这个故事的文本中删除所有形状。 |
| [EnsureMinimum](../../aspose.words/body/ensureminimum)() | 如果最后一个孩子不是段落，则创建并附加一个空段落。 |
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

**正文** 可以包含 **段落** 和 **表** 子节点。

**Body** 是节级节点，只能是 **的子节点 部分** 。  **Section** 中只能有一个 **Body** 。

最小有效 **正文** 需要包含至少一个 **段落** 。

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

* class [Story](../story)
* 命名空间 [Aspose.Words](../../aspose.words)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
