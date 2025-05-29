---
title: Paragraph Class
linktitle: Paragraph
articleTitle: Paragraph
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Paragraph 类，轻松管理和格式化文本段落，增强您的文档处理能力。
type: docs
weight: 5120
url: /zh/net/aspose.words/paragraph/
---
## Paragraph class

代表一段文字。

要了解更多信息，请访问[使用段落](https://docs.aspose.com/words/net/working-with-paragraphs/)文档文章。

```csharp
public class Paragraph : CompositeNode
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [Paragraph](paragraph/)(*[DocumentBase](../documentbase/)*) | 初始化`Paragraph`类. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator/) { get; } | 如果此段落分隔符是样式分隔符，则为 True。样式分隔符允许一个 段落由具有不同段落样式的部分组成。 |
| [Count](../../aspose.words/compositenode/count/) { get; } | 获取此节点的直属子节点的数量。 |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取此节点所属的文档。 |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | 获取节点的第一个子节点。 |
| [FrameFormat](../../aspose.words/paragraph/frameformat/) { get; } | 提供对框架格式属性的访问。 |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | 返回`真的`如果此节点有任何子节点。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | 返回`真的`因为这个节点可以有子节点。 |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision/) { get; } | 如果在启用更改跟踪的情况下在 Microsoft Word 中删除了此对象，则返回 true。 |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell/) { get; } | 如果此段是[`Cell`](../../aspose.words.tables/cell/) ；否则为假。 |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument/) { get; } | 如果此段是文档最后一节的最后一段，则为真。 |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter/) { get; } | 如果此段是段落的最后一段，则为 True[`HeaderFooter`](../headerfooter/) （正文故事）[`Section`](../section/) ；否则为假。 |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection/) { get; } | 如果此段是段落的最后一段，则为 True[`Body`](../body/) （正文故事）[`Section`](../section/) ；否则为假。 |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision/) { get; } | 如果在启用更改跟踪的情况下 Microsoft Word 中的对象格式发生更改，则返回 true。 |
| [IsInCell](../../aspose.words/paragraph/isincell/) { get; } | 如果此段落是其直接子段落，则为 True[`Cell`](../../aspose.words.tables/cell/) ；否则为假。 |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision/) { get; } | 如果在启用更改跟踪的情况下将此对象插入 Microsoft Word，则返回 true。 |
| [IsListItem](../../aspose.words/paragraph/islistitem/) { get; } | 当段落是原始修订中的项目符号或编号列表中的项目时，为真。 |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision/) { get; } | 返回`真的`如果在启用更改跟踪的情况下在 Microsoft Word 中移动（删除）此对象。 |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision/) { get; } | 返回`真的`如果在启用更改跟踪的情况下在 Microsoft Word 中移动（插入）此对象。 |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | 获取节点的最后一个子节点。 |
| [ListFormat](../../aspose.words/paragraph/listformat/) { get; } | 提供对段落列表格式属性的访问。 |
| [ListLabel](../../aspose.words/paragraph/listlabel/) { get; } | 获得[`ListLabel`](./listlabel/)提供对列表编号值和此段落的格式 的访问的对象。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随此节点之后的节点。 |
| override [NodeType](../../aspose.words/paragraph/nodetype/) { get; } | 返回Paragraph. |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont/) { get; } | 提供对段落分隔符的字体格式的访问。 |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat/) { get; } | 提供对段落格式属性的访问。 |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [ParentSection](../../aspose.words/paragraph/parentsection/) { get; } | 检索父级[`Section`](../section/)段落。 |
| [ParentStory](../../aspose.words/paragraph/parentstory/) { get; } | 检索可[`Body`](../body/)或者[`HeaderFooter`](../headerfooter/). |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取此节点前一个节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回[`Range`](../range/)表示此节点中包含的文档部分的对象。 |
| [Runs](../../aspose.words/paragraph/runs/) { get; } | 提供对段落内文本片段的键入集合的访问。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept/)(*[DocumentVisitor](../documentvisitor/)*) | 接受访客。 |
| override [AcceptEnd](../../aspose.words/paragraph/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | 接受访问者访问文档段落的末尾。 |
| override [AcceptStart](../../aspose.words/paragraph/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | 接受访问者访问文档段落的开头。 |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_1)(*string*) | 将字段附加到此段落。 |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool*) | 将字段附加到此段落。 |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_2)(*string, string*) | 将字段附加到此段落。 |
| [Clone](../../aspose.words/node/clone/)(*bool*) | 创建节点的副本。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | 创建可用于遍历和读取节点的导航器。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | 获取指定的第一个祖先[`NodeType`](../nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | 获取指定对象类型的第一个祖先。 |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | 返回与指定类型匹配的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops/)() | 返回应用于此段落的所有制表位数组，包括通过样式或列表间接应用的制表位。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | 为该节点的子节点提供对每个样式迭代的支持。 |
| override [GetText](../../aspose.words/paragraph/gettext/)() | 获取此段落的文本（包括段落结束字符）。 |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | 返回子节点数组中指定子节点的索引。 |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | 在指定的参考节点后立即插入指定的节点。 |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | 在指定的参考节点之前立即插入指定的节点。 |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_1)(*string, [Node](../node/), bool*) | 在此段落中插入一个字段。 |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool, [Node](../node/), bool*) | 在此段落中插入一个字段。 |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_2)(*string, string, [Node](../node/), bool*) | 在此段落中插入一个字段。 |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting/)() | 连接段落中具有相同格式的运行。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | 根据前序树遍历算法获取下一个节点。 |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | 将指定节点添加到此节点的子节点列表的开头。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | 根据前序树遍历算法获取前一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 将自身从父级中移除。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | 删除当前节点的所有子节点。 |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | 删除指定的子节点。 |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | 删除所有[`SmartTag`](../../aspose.words.markup/smarttag/)当前节点的后代节点。 |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | 选择与 XPath 表达式匹配的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | 选择第一个[`Node`](../node/)与 XPath 表达式匹配。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的保存选项将节点内容导出为字符串。 |

## 评论

`Paragraph`是块级节点，可以是派生自 的类的子类[`Story`](../story/)或者[`InlineStory`](../inlinestory/)。

`Paragraph`可以包含任意数量的内联级节点和书签。

段落内可出现的子节点的完整列表包括 [`BookmarkStart`](../bookmarkstart/)，[`BookmarkEnd`](../bookmarkend/), [`FieldStart`](../../aspose.words.fields/fieldstart/)，[`FieldSeparator`](../../aspose.words.fields/fieldseparator/), [`FieldEnd`](../../aspose.words.fields/fieldend/)，[`FormField`](../../aspose.words.fields/formfield/), [`Comment`](../comment/)，[`Footnote`](../../aspose.words.notes/footnote/), [`Run`](../run/)，[`SpecialChar`](../specialchar/), [`Shape`](../../aspose.words.drawing/shape/)，[`GroupShape`](../../aspose.words.drawing/groupshape/), [`SmartTag`](../../aspose.words.markup/smarttag/)。

Microsoft Word 中的有效段落始终以段落分隔符结尾，并且 最小有效段落仅由段落分隔符组成。`Paragraph` 类会自动在末尾添加适当的段落分隔符 ，并且该字符不是`Paragraph`，因此 a`Paragraph`可以为空。

不包括段落结尾[`ParagraphBreak`](../controlchar/paragraphbreak/) 或单元格结尾[`Cell`](../controlchar/cell/)段落文本中的字符，因为当在 Microsoft Word 中打开文档时，它可能会使段落无效。

## 例子

展示如何手动构建 Aspose.Words 文档。

```csharp
Document doc = new Document();

// 一个空白文档包含一个部分、一个正文和一个段落。
// 调用“RemoveAllChildren”方法删除所有节点，
// 并最终得到一个没有子节点的文档节点。
doc.RemoveAllChildren();

// 此文档现在没有可以添加内容的复合子节点。
// 如果我们想要编辑它，我们将需要重新填充它的节点集合。
// 首先，创建一个新的部分，然后将其作为子节点附加到根文档节点。
Section section = new Section(doc);
doc.AppendChild(section);

// 为该部分设置一些页面设置属性。
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// 一个部分需要一个主体，它将包含并显示其所有内容
// 位于页面部分页眉和页脚之间。
Body body = new Body(doc);
section.AppendChild(body);

// 创建一个段落，设置一些格式属性，然后将其作为子部分附加到正文中。
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// 最后，添加一些内容来执行文档。创建一个运行，
// 设置其外观和内容，然后将其作为子项附加到段落。
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
