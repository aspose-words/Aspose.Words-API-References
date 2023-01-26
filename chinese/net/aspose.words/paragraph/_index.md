---
title: Paragraph
second_title: Aspose.Words for .NET API 参考
description: 代表一段文字
type: docs
weight: 4150
url: /zh/net/aspose.words/paragraph/
---
## Paragraph class

代表一段文字。

```csharp
public class Paragraph : CompositeNode
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [Paragraph](paragraph/)(DocumentBase) | 初始化 **段落**类. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator/) { get; } | 如果此段落分隔符是样式分隔符，则为真。样式分隔符允许一个 段落由具有不同段落样式的部分组成。 |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | 获取该节点的所有直接子节点。 |
| [Count](../../aspose.words/compositenode/count/) { get; } | 获取此节点的直接子节点数。 |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取该节点所属的文档。 |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | 获取节点的第一个子节点。 |
| [FrameFormat](../../aspose.words/paragraph/frameformat/) { get; } | 提供对段落格式属性的访问。 |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | 如果此节点有任何子节点，则返回 true。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | 返回真，因为该节点可以有子节点。 |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision/) { get; } | 如果在启用更改跟踪时在 Microsoft Word 中删除了此对象，则返回 true。 |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell/) { get; } | 如果本段是最后一段，则为真[`Cell`](../../aspose.words.tables/cell/);否则为假。 |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument/) { get; } | 如果此段落是文档最后一段中的最后一段，则为真。 |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter/) { get; } | 如果本段是最后一段，则为真 **页眉页脚**（正文故事） **部分**;否则为假。 |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection/) { get; } | 如果本段是最后一段，则为真 **身体**（正文故事） **部分**;否则为假。 |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision/) { get; } | 如果启用更改跟踪时在 Microsoft Word 中更改了对象的格式，则返回 true。 |
| [IsInCell](../../aspose.words/paragraph/isincell/) { get; } | 如果此段落是[`Cell`](../../aspose.words.tables/cell/);否则为假。 |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision/) { get; } | 如果在启用更改跟踪时将此对象插入 Microsoft Word，则返回 true。 |
| [IsListItem](../../aspose.words/paragraph/islistitem/) { get; } | 当段落是原始版本的项目符号或编号列表中的项目时为真。 |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision/) { get; } | 返回 **真的**如果启用更改跟踪时此对象在 Microsoft Word 中被移动（删除）。 |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision/) { get; } | 返回 **真的**如果启用更改跟踪时在 Microsoft Word 中移动（插入）此对象。 |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | 获取节点的最后一个子节点。 |
| [ListFormat](../../aspose.words/paragraph/listformat/) { get; } | 提供对段落列表格式属性的访问。 |
| [ListLabel](../../aspose.words/paragraph/listlabel/) { get; } | 得到一个[`ListLabel`](./listlabel/)提供对该段落的列表编号值和格式化 的访问的对象。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧跟此节点的节点。 |
| override [NodeType](../../aspose.words/paragraph/nodetype/) { get; } | 返回 **节点类型.段落**. |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont/) { get; } | 提供对分段符的字体格式的访问。 |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat/) { get; } | 提供对段落格式属性的访问。 |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [ParentSection](../../aspose.words/paragraph/parentsection/) { get; } | 检索父级[`Section`](../section/)段落的. |
| [ParentStory](../../aspose.words/paragraph/parentstory/) { get; } | 检索父节级故事，可以[`Body`](../body/)或者[`HeaderFooter`](../headerfooter/). |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取紧接在此节点之前的节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回一个 **范围**表示此节点中包含的文档部分的对象。 |
| [Runs](../../aspose.words/paragraph/runs/) { get; } | 提供对段落内文本片段的类型化集合的访问。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept/)(DocumentVisitor) | 接受访客。 |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | 将指定节点添加到该节点的子节点列表的末尾。 |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_1)(string) | 将一个字段附加到本段。 |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield)(FieldType, bool) | 将一个字段附加到本段。 |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_2)(string, string) | 将一个字段附加到本段。 |
| [Clone](../../aspose.words/node/clone/)(bool) | 创建节点的副本。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | 保留供系统使用。 IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | 获取指定的第一个祖先[`NodeType`](../nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | 获取指定对象类型的第一个祖先。 |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | 返回与指定类型匹配的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops/)() | 返回应用于此段落的所有制表位的数组，包括由样式或列表间接应用的。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | 为在该节点的子节点上的每个样式迭代提供支持。 |
| override [GetText](../../aspose.words/paragraph/gettext/)() | 获取该段落的文本，包括段落结尾字符。 |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | 返回子节点数组中指定子节点的索引。 |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | 在指定参考节点之后立即插入指定节点。 |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | 在指定的参考节点之前插入指定的节点。 |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_1)(string, Node, bool) | 在本段中插入一个字段。 |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield)(FieldType, bool, Node, bool) | 在本段中插入一个字段。 |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_2)(string, string, Node, bool) | 在本段中插入一个字段。 |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting/)() | 以段落中相同的格式连接运行。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | 根据前序树遍历算法获取下一个节点。 |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | 将指定节点添加到此节点的子节点列表的开头。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | 根据前序树遍历算法获取上一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 从父级中移除自身。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | 移除当前节点的所有子节点。 |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | 移除指定的子节点。 |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | 删除所有[`SmartTag`](../../aspose.words.markup/smarttag/)当前节点的后代节点。 |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | 选择与 XPath 表达式匹配的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | 选择与 XPath 表达式匹配的第一个节点。 |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | 使用指定的保存选项将节点的内容导出为字符串。 |

### 评论

`Paragraph`是块级节点，可以是派生自 的类的子节点[`Story`](../story/)或者[`InlineStory`](../inlinestory/).

`Paragraph`可以包含任意数量的内联级节点和书签。

段落中可能出现的子节点的完整列表包括 [`BookmarkStart`](../bookmarkstart/),[`BookmarkEnd`](../bookmarkend/), [`FieldStart`](../../aspose.words.fields/fieldstart/),[`FieldSeparator`](../../aspose.words.fields/fieldseparator/), [`FieldEnd`](../../aspose.words.fields/fieldend/),[`FormField`](../../aspose.words.fields/formfield/), [`Comment`](../comment/),[`Footnote`](../../aspose.words.notes/footnote/), [`Run`](../run/),[`SpecialChar`](../specialchar/), [`Shape`](../../aspose.words.drawing/shape/),[`GroupShape`](../../aspose.words.drawing/groupshape/), [`SmartTag`](../../aspose.words.markup/smarttag/).

Microsoft Word 中的有效段落始终以段落分隔符结尾，并且 最小有效段落仅包含段落分隔符。这 **段落** 类自动在 end 处附加适当的分节符，并且该字符不是子节点的一部分 **段落**，因此 a **段落**可以为空。

不包括段落结尾[`ControlChar.ParagraphBreak`](../controlchar/paragraphbreak/) 或单元格结尾[`控制字符单元`](../controlchar/cell/) 段落文本中的字符，因为当在 Microsoft Word 中打开文档时，它可能使段落无效。

### 例子

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

### 也可以看看

* class [CompositeNode](../compositenode/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
