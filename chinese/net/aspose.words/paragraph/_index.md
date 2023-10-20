---
title: Paragraph Class
linktitle: Paragraph
articleTitle: Paragraph
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Paragraph 班级. 代表一段文本 在 C#.
type: docs
weight: 4390
url: /zh/net/aspose.words/paragraph/
---
## Paragraph class

代表一段文本。

要了解更多信息，请访问[使用段落](https://docs.aspose.com/words/net/working-with-paragraphs/)文档文章。

```csharp
public class Paragraph : CompositeNode
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [Paragraph](paragraph/)(*[DocumentBase](../documentbase/)*) | 初始化一个新实例`Paragraph`类. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator/) { get; } | 如果此段落分隔符是样式分隔符，则为 True。样式分隔符允许 one 段落由具有不同段落样式的部分组成。 |
| [Count](../../aspose.words/compositenode/count/) { get; } | 获取此节点的直接子节点的数量。 |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取该节点所属的文档。 |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | 获取节点的第一个子节点。 |
| [FrameFormat](../../aspose.words/paragraph/frameformat/) { get; } | 提供对帧格式属性的访问。 |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | 返回`真的`如果该节点有任何子节点. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | 返回`真的`因为该节点可以有子节点。 |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision/) { get; } | 如果在启用更改跟踪时在 Microsoft Word 中删除了此对象，则返回 true。 |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell/) { get; } | 如果该段落是最后一段，则为 True[`Cell`](../../aspose.words.tables/cell/);否则为假。 |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument/) { get; } | 如果该段落是文档最后一部分的最后一段，则为 True。 |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter/) { get; } | 如果该段落是最后一段，则为 True[`HeaderFooter`](../headerfooter/) （正文故事）a[`Section`](../section/);否则为假。 |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection/) { get; } | 如果该段落是最后一段，则为 True[`Body`](../body/) （正文故事）a[`Section`](../section/);否则为假。 |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision/) { get; } | 如果在启用更改跟踪的情况下在 Microsoft Word 中更改了对象的格式，则返回 true。 |
| [IsInCell](../../aspose.words/paragraph/isincell/) { get; } | 如果该段落是以下段落的直接子段落，则为真[`Cell`](../../aspose.words.tables/cell/);否则为假。 |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision/) { get; } | 如果在启用更改跟踪的情况下将此对象插入到 Microsoft Word 中，则返回 true。 |
| [IsListItem](../../aspose.words/paragraph/islistitem/) { get; } | 当该段落是原始版本中项目符号列表或编号列表中的项目时为真。 |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision/) { get; } | 返回`真的`如果启用更改跟踪时在 Microsoft Word 中移动（删除）此对象。 |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision/) { get; } | 返回`真的`如果在启用更改跟踪的情况下在 Microsoft Word 中移动（插入）此对象。 |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | 获取节点的最后一个子节点。 |
| [ListFormat](../../aspose.words/paragraph/listformat/) { get; } | 提供对段落的列表格式属性的访问。 |
| [ListLabel](../../aspose.words/paragraph/listlabel/) { get; } | 获得[`ListLabel`](./listlabel/)提供对此段落的列表编号值和格式 的访问的对象。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随该节点的下一个节点。 |
| override [NodeType](../../aspose.words/paragraph/nodetype/) { get; } | 返回Paragraph. |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont/) { get; } | 提供对段落分隔符的字体格式的访问。 |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat/) { get; } | 提供对段落格式属性的访问。 |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [ParentSection](../../aspose.words/paragraph/parentsection/) { get; } | 检索父级[`Section`](../section/)该段落的. |
| [ParentStory](../../aspose.words/paragraph/parentstory/) { get; } | 检索父部分级别的故事，可以[`Body`](../body/)或者[`HeaderFooter`](../headerfooter/). |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取紧邻此节点之前的节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回一个[`Range`](../range/)表示此节点中包含的文档部分的对象。 |
| [Runs](../../aspose.words/paragraph/runs/) { get; } | 提供对段落内文本片段的键入集合的访问。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept/)(*[DocumentVisitor](../documentvisitor/)*) | 接受访客。 |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../node/)*) | 将指定节点添加到该节点的子节点列表的末尾。 |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_1)(*string*) | 将字段附加到此段落。 |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool*) | 将字段附加到此段落。 |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_2)(*string, string*) | 将字段附加到此段落。 |
| [Clone](../../aspose.words/node/clone/)(*bool*) | 创建节点的副本。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | 创建可用于遍历和读取节点的导航器。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | 获取指定的第一个祖先[`NodeType`](../nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | 获取指定对象类型的第一个祖先。 |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | 返回与指定类型匹配的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops/)() | 返回应用于此段落的所有制表位的数组，包括通过样式或列表间接应用的。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | 为该节点的子节点上的每个样式迭代提供支持。 |
| override [GetText](../../aspose.words/paragraph/gettext/)() | 获取该段落的文本，包括段落结尾字符。 |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | 返回子节点数组中指定子节点的索引。 |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../node/), [Node](../node/)*) | 在指定的引用节点之后立即插入指定的节点。 |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../node/), [Node](../node/)*) | 在指定的引用节点之前插入指定的节点。 |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_1)(*string, [Node](../node/), bool*) | 在该段落中插入一个字段。 |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool, [Node](../node/), bool*) | 在该段落中插入一个字段。 |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_2)(*string, string, [Node](../node/), bool*) | 在该段落中插入一个字段。 |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting/)() | 连接段落中具有相同格式的运行。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | 根据先序树遍历算法获取下一个节点。 |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../node/)*) | 将指定节点添加到该节点的子节点列表的开头。 |
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

`Paragraph`是块级节点，可以是派生自 的类的子节点[`Story`](../story/)或者[`InlineStory`](../inlinestory/)。

`Paragraph`可以包含任意数量的内联级节点和书签。

段落内可能出现的子节点的完整列表由 组成[`BookmarkStart`](../bookmarkstart/),[`BookmarkEnd`](../bookmarkend/), [`FieldStart`](../../aspose.words.fields/fieldstart/),[`FieldSeparator`](../../aspose.words.fields/fieldseparator/), [`FieldEnd`](../../aspose.words.fields/fieldend/),[`FormField`](../../aspose.words.fields/formfield/), [`Comment`](../comment/),[`Footnote`](../../aspose.words.notes/footnote/), [`Run`](../run/),[`SpecialChar`](../specialchar/), [`Shape`](../../aspose.words.drawing/shape/),[`GroupShape`](../../aspose.words.drawing/groupshape/), [`SmartTag`](../../aspose.words.markup/smarttag/)。

Microsoft Word 中的有效段落始终以段落分隔符结尾，并且 最小有效段落仅包含段落分隔符。这`Paragraph` 类自动在 end 处附加适当的段落分隔符，并且该字符不是 类的子节点的一部分`Paragraph`，因此 a`Paragraph`可以为空。

不包括段落结尾[`ParagraphBreak`](../controlchar/paragraphbreak/) 或单元格末尾[`Cell`](../controlchar/cell/)段落文本中的字符，因为在 Microsoft Word 中打开文档时，这可能会使段落无效。

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
