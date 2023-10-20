---
title: StructuredDocumentTag Class
linktitle: StructuredDocumentTag
articleTitle: StructuredDocumentTag
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Markup.StructuredDocumentTag 班级. 表示文档中的结构化文档标签SDT 或内容控件 在 C#.
type: docs
weight: 4060
url: /zh/net/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class

表示文档中的结构化文档标签（SDT 或内容控件）。

```csharp
public class StructuredDocumentTag : CompositeNode, IStructuredDocumentTag
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [StructuredDocumentTag](structureddocumenttag/)(*[DocumentBase](../../aspose.words/documentbase/), [SdtType](../sdttype/), [MarkupLevel](../markuplevel/)*) | 初始化**结构化文档标签**类. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttag/appearance/) { get; set; } | 获取/设置结构化文档标签的外观。 |
| [BuildingBlockCategory](../../aspose.words.markup/structureddocumenttag/buildingblockcategory/) { get; set; } | 为此指定构建块的类别**SDT**node. 不能为空。 |
| [BuildingBlockGallery](../../aspose.words.markup/structureddocumenttag/buildingblockgallery/) { get; set; } | 为此指定构建块的类型**SDT** 不能为空。 |
| [CalendarType](../../aspose.words.markup/structureddocumenttag/calendartype/) { get; set; } | 为此指定日历的类型**SDT**. 默认为Default |
| [Checked](../../aspose.words.markup/structureddocumenttag/checked/) { get; set; } | 获取/设置复选框的当前状态**SDT**. 此属性的默认值为 false。 |
| [Color](../../aspose.words.markup/structureddocumenttag/color/) { get; set; } | 获取或设置结构化文档标签的颜色。 |
| [ContentsFont](../../aspose.words.markup/structureddocumenttag/contentsfont/) { get; } | 将应用于输入文本的字体格式**SDT**. |
| [Count](../../aspose.words/compositenode/count/) { get; } | 获取此节点的直接子节点数。 |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| [DateDisplayFormat](../../aspose.words.markup/structureddocumenttag/datedisplayformat/) { get; set; } | 表示日期显示格式的字符串。 不能为空。 英语（美国）的日期是“mm/dd/yyyy” |
| [DateDisplayLocale](../../aspose.words.markup/structureddocumenttag/datedisplaylocale/) { get; set; } | 允许设置/获取在此显示的日期的语言格式**SDT**. |
| [DateStorageFormat](../../aspose.words.markup/structureddocumenttag/datestorageformat/) { get; set; } | 获取/设置日期 SDT 的日期存储格式，当**SDT**绑定到文档数据存储中的 XML 节点。 默认值为DateTime |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取该节点所属的文档。 |
| [EndCharacterFont](../../aspose.words.markup/structureddocumenttag/endcharacterfont/) { get; } | 将应用于输入文本的最后一个字符的字体格式**SDT**. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | 获取节点的第一个子节点。 |
| [FullDate](../../aspose.words.markup/structureddocumenttag/fulldate/) { get; set; } | 指定上次输入的完整日期和时间**SDT**. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | 如果此节点有任何子节点，则返回 true。 |
| [Id](../../aspose.words.markup/structureddocumenttag/id/) { get; } | 为此指定一个唯一的只读持久数字 ID**SDT**. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | 返回真，因为该节点可以有子节点。 |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttag/isshowingplaceholdertext/) { get; set; } | 指定此内容是否**SDT**应被解释为包含占位符 text （与 SDT 中的常规文本内容相反）。 |
| [IsTemporary](../../aspose.words.markup/structureddocumenttag/istemporary/) { get; set; } | 指定这是否**SDT**当其 contents 被修改时，应从 WordProcessingML 文档中删除。 |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | 获取节点的最后一个子节点。 |
| [Level](../../aspose.words.markup/structureddocumenttag/level/) { get; } | 获取这个级别**SDT**出现在文档树中。 |
| [ListItems](../../aspose.words.markup/structureddocumenttag/listitems/) { get; } | 获取[`SdtListItemCollection`](../sdtlistitemcollection/)与此相关**SDT** |
| [LockContentControl](../../aspose.words.markup/structureddocumenttag/lockcontentcontrol/) { get; set; } | 当设置为 true 时，此属性将禁止用户删除此**SDT**. |
| [LockContents](../../aspose.words.markup/structureddocumenttag/lockcontents/) { get; set; } | 当设置为 true 时，此属性将禁止用户编辑此内容**SDT**. |
| [Multiline](../../aspose.words.markup/structureddocumenttag/multiline/) { get; set; } | 指定这是否**SDT**允许多行文本。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧跟此节点的节点。 |
| override [NodeType](../../aspose.words.markup/structureddocumenttag/nodetype/) { get; } | 返回**NodeType.StructuredDocumentTag**. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [Placeholder](../../aspose.words.markup/structureddocumenttag/placeholder/) { get; } | 获取[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)包含当此 SDT 运行内容为空时应显示的占位符文本， 关联的映射 XML 元素为空，如通过[`XmlMapping`](./xmlmapping/)element 或[`IsShowingPlaceholderText`](./isshowingplaceholdertext/)元素为真。 |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttag/placeholdername/) { get; set; } | 获取或设置名称[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)包含占位符文本。 |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取紧接在此节点之前的节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回一个**范围**表示此节点中包含的文档部分的对象。 |
| [SdtType](../../aspose.words.markup/structureddocumenttag/sdttype/) { get; } | 获取 this 的类型**结构化文档标签**. |
| [Style](../../aspose.words.markup/structureddocumenttag/style/) { get; set; } | 获取或设置结构化文档标签的样式。 |
| [StyleName](../../aspose.words.markup/structureddocumenttag/stylename/) { get; set; } | 获取或设置应用于结构化文档标签的样式名称。 |
| [Tag](../../aspose.words.markup/structureddocumenttag/tag/) { get; set; } | 指定与当前 SDT 节点关联的标签。 不能为空。 |
| [Title](../../aspose.words.markup/structureddocumenttag/title/) { get; set; } | 指定与此关联的友好名称**SDT**. 不能为空。 |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttag/wordopenxml/) { get; } | 获取一个字符串，该字符串表示包含在FlatOpc格式. |
| [WordOpenXMLMinimal](../../aspose.words.markup/structureddocumenttag/wordopenxmlminimal/) { get; } |  |
| [XmlMapping](../../aspose.words.markup/structureddocumenttag/xmlmapping/) { get; } | 获取一个对象，该对象表示此结构化文档标记到当前文档的自定义 XML 部分中的 XML 数据 的映射。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttag/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | 接受访客。 |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../../aspose.words/node/)*) | 将指定节点添加到该节点的子节点列表的末尾。 |
| [Clear](../../aspose.words.markup/structureddocumenttag/clear/)() | 清除此结构化文档标记的内容并显示占位符（如果已定义）。 |
| [Clone](../../aspose.words/node/clone/)(*bool*) | 创建节点的副本。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | 保留供系统使用。 IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | 获取指定的第一个祖先[`NodeType`](../../aspose.words/nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | 获取指定对象类型的第一个祖先。 |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | 返回与指定类型匹配的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | 为在该节点的子节点上的每个样式迭代提供支持。 |
| override [GetText](../../aspose.words/compositenode/gettext/)() | 获取该节点及其所有子节点的文本。 |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | 返回子节点数组中指定子节点的索引。 |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | 在指定参考节点之后立即插入指定节点。 |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | 在指定的参考节点之前插入指定的节点。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | 根据前序树遍历算法获取下一个节点。 |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../../aspose.words/node/)*) | 将指定节点添加到此节点的子节点列表的开头。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | 根据前序树遍历算法获取上一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 从父级中移除自身。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | 移除当前节点的所有子节点。 |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../../aspose.words/node/)*) | 移除指定的子节点。 |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttag/removeselfonly/)() | 仅删除此 SDT 节点本身，但将其内容保留在文档树中。 |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | 删除所有[`SmartTag`](../smarttag/)当前节点的后代节点。 |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | 选择与 XPath 表达式匹配的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | 选择与 XPath 表达式匹配的第一个节点。 |
| [SetCheckedSymbol](../../aspose.words.markup/structureddocumenttag/setcheckedsymbol/)(*int, string*) | 设置用于表示复选框内容控件的选中状态的符号。 |
| [SetUncheckedSymbol](../../aspose.words.markup/structureddocumenttag/setuncheckedsymbol/)(*int, string*) | 设置用于表示复选框内容控件的未选中状态的符号。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的保存选项将节点的内容导出为字符串。 |

## 评论

结构化文档标签 (SDT) 允许将客户定义的语义及其 行为和外观嵌入到文档中。

在这个版本中，Aspose.Words 提供了许多公共方法和属性来 操纵行为和内容`StructuredDocumentTag` 可以使用 将 SDT 节点映射到文档中的自定义 XML 包[`XmlMapping`](./xmlmapping/)财产。

`StructuredDocumentTag`可能出现在文档中的以下位置：

* 块级 - 在段落和表格中，作为 a 的子级[`Body`](../../aspose.words/body/),[`HeaderFooter`](../../aspose.words/headerfooter/)[`Comment`](../../aspose.words/comment/),[`Footnote`](../../aspose.words.notes/footnote/)或一个[`Shape`](../../aspose.words.drawing/shape/)节点。
* 行级 - 在表中的行中，作为[`Table`](../../aspose.words.tables/table/)节点。
* 单元格级别 - 在表格行中的单元格中，作为[`Row`](../../aspose.words.tables/row/)节点。
* Inline-level - 在里面的内联内容中，作为一个子级[`Paragraph`](../../aspose.words/paragraph/).
* 嵌套在另一个里面`StructuredDocumentTag`.

## 例子

展示如何使用内容控制元素的样式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 以下是将文档中的样式应用到结构化文档标签的两种方法。
// 1 - 应用文档样式集合中的样式对象：
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - 按名称引用文档中的样式：
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### 也可以看看

* class [CompositeNode](../../aspose.words/compositenode/)
* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* 命名空间 [Aspose.Words.Markup](../../aspose.words.markup/)
* 部件 [Aspose.Words](../../)
