---
title: StructuredDocumentTag
second_title: Aspose.Words for .NET API 参考
description: 表示文档中的结构化文档标签SDT 或内容控件
type: docs
weight: 3770
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
| [StructuredDocumentTag](structureddocumenttag)(DocumentBase, SdtType, MarkupLevel) | 初始化 **结构化文档标签** 类的新实例。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttag/appearance) { get; set; } | 获取/设置结构化文档标签的外观。 |
| [BuildingBlockCategory](../../aspose.words.markup/structureddocumenttag/buildingblockcategory) { get; set; } | 指定此 **SDT** 节点的构建块类别。 不能为空。 |
| [BuildingBlockGallery](../../aspose.words.markup/structureddocumenttag/buildingblockgallery) { get; set; } | 指定此 **SDT** 的构建块类型。 不能为空。 |
| [CalendarType](../../aspose.words.markup/structureddocumenttag/calendartype) { get; set; } | 指定此 **SDT** 的日历类型。 默认为Default |
| [Checked](../../aspose.words.markup/structureddocumenttag/checked) { get; set; } | 获取/设置复选框 **SDT** 的当前状态。 此属性的默认值为 false。 |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | 获取该节点的所有直接子节点。 |
| [Color](../../aspose.words.markup/structureddocumenttag/color) { get; set; } | 获取或设置结构化文档标签的颜色。 |
| [ContentsFont](../../aspose.words.markup/structureddocumenttag/contentsfont) { get; } | 将应用于输入到 **SDT** 的文本的字体格式。 |
| [Count](../../aspose.words/compositenode/count) { get; } | 获取此节点的直接子节点数。 |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | 指定自定义节点标识符。 |
| [DateDisplayFormat](../../aspose.words.markup/structureddocumenttag/datedisplayformat) { get; set; } | 表示日期显示格式的字符串。 不能为空。  英语（美国）的日期是“mm/dd/yyyy” |
| [DateDisplayLocale](../../aspose.words.markup/structureddocumenttag/datedisplaylocale) { get; set; } | 允许设置/获取此 **SDT** 中显示的日期的语言格式。 |
| [DateStorageFormat](../../aspose.words.markup/structureddocumenttag/datestorageformat) { get; set; } | 获取/设置在绑定 **SDT** 时存储日期 SDT 的日期格式到文档数据存储中的 XML 节点。 默认值为DateTime |
| virtual [Document](../../aspose.words/node/document) { get; } | 获取该节点所属的文档。 |
| [EndCharacterFont](../../aspose.words.markup/structureddocumenttag/endcharacterfont) { get; } | 将应用于输入 **SDT** 的文本的最后一个字符的字体格式。 |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | 获取节点的第一个子节点。 |
| [FullDate](../../aspose.words.markup/structureddocumenttag/fulldate) { get; set; } | 指定上次输入此 **SDT** 的完整日期和时间。 |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | 如果此节点有任何子节点，则返回 true。 |
| [Id](../../aspose.words.markup/structureddocumenttag/id) { get; } | 为此 **SDT** 指定唯一的只读持久数字 ID。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | 返回真，因为该节点可以有子节点。 |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttag/isshowingplaceholdertext) { get; set; } | 指定此 **SDT** 的内容是否应解释为包含占位符文本 （与 SDT 中的常规文本内容相反）。 |
| [IsTemporary](../../aspose.words.markup/structureddocumenttag/istemporary) { get; set; } | 指定此 **SDT** 在其内容 时是否应从 WordProcessingML 文档中删除被修改。 |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | 获取节点的最后一个子节点。 |
| [Level](../../aspose.words.markup/structureddocumenttag/level) { get; } | 获取此 **SDT** 在文档树中出现的级别。 |
| [ListItems](../../aspose.words.markup/structureddocumenttag/listitems) { get; } | 获取[`SdtListItemCollection`](../sdtlistitemcollection)与此关联 **SDT** 。 |
| [LockContentControl](../../aspose.words.markup/structureddocumenttag/lockcontentcontrol) { get; set; } | 设置为 true 时，此属性将禁止用户删除此 **SDT** 。 |
| [LockContents](../../aspose.words.markup/structureddocumenttag/lockcontents) { get; set; } | 当设置为 true 时，此属性将禁止用户编辑此 **SDT** 的内容。 |
| [Multiline](../../aspose.words.markup/structureddocumenttag/multiline) { get; set; } | 指定此 **SDT** 是否允许多行文本。 |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | 获取紧跟该节点的节点。 |
| override [NodeType](../../aspose.words.markup/structureddocumenttag/nodetype) { get; } | 返回 **NodeType.StructuredDocumentTag** 。 |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | 获取此节点的直接父节点。 |
| [Placeholder](../../aspose.words.markup/structureddocumenttag/placeholder) { get; } | 获取[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock)包含在此 SDT 运行内容为空时应显示的占位符文本， 关联的映射 XML 元素为空，如通过[`XmlMapping`](./xmlmapping)元素 或:::R5 指定:P:Aspose.Words.Markup.StructuredDocumentTag.IsShowingPlaceholderText:::元素为真。 |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttag/placeholdername) { get; set; } | 获取或设置包含占位符文本的[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock)的名称。 |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | 获取紧接在此节点之前的节点。 |
| [Range](../../aspose.words/node/range) { get; } | 返回 **Range** 对象，该对象表示包含在此节点中的文档部分。 |
| [SdtType](../../aspose.words.markup/structureddocumenttag/sdttype) { get; } | 获取此 **结构化文档标签** 的类型。 |
| [Style](../../aspose.words.markup/structureddocumenttag/style) { get; set; } | 获取或设置结构化文档标签的样式。 |
| [StyleName](../../aspose.words.markup/structureddocumenttag/stylename) { get; set; } | 获取或设置应用于结构化文档标签的样式名称。 |
| [Tag](../../aspose.words.markup/structureddocumenttag/tag) { get; set; } | 指定与当前 SDT 节点关联的标签。 不能为空。 |
| [Title](../../aspose.words.markup/structureddocumenttag/title) { get; set; } | 指定与此 **SDT** 关联的友好名称。 不能为空。 |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttag/wordopenxml) { get; } | 获取一个字符串，该字符串表示包含在FlatOpc格式的节点中的 XML。 |
| [XmlMapping](../../aspose.words.markup/structureddocumenttag/xmlmapping) { get; } | 获取一个对象，该对象表示此结构化文档标记到当前文档的自定义 XML 部分中的 XML 数据 的映射。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttag/accept)(DocumentVisitor) | 接受访问者。 |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [Clear](../../aspose.words.markup/structureddocumenttag/clear)() | 清除此结构化文档标记的内容并显示占位符（如果已定义）。 |
| [Clone](../../aspose.words/node/clone)(bool) | 创建节点的副本。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | 保留供系统使用。 IXPath 可导航。 |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | 获取指定[`NodeType`](../../aspose.words/nodetype)的第一个祖先。 |
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
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttag/removeselfonly)() | 仅删除此 SDT 节点本身，但将其内容保留在文档树中。 |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | 删除当前节点的所有[`SmartTag`](../smarttag)后代节点。 |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | 选择与 XPath 表达式匹配的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | 选择与 XPath 表达式匹配的第一个节点。 |
| [SetCheckedSymbol](../../aspose.words.markup/structureddocumenttag/setcheckedsymbol)(int, string) | 设置用于表示复选框内容控件的选中状态的符号。 |
| [SetUncheckedSymbol](../../aspose.words.markup/structureddocumenttag/setuncheckedsymbol)(int, string) | 设置用于表示复选框内容控件的未选中状态的符号。 |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | 使用指定的保存选项将节点的内容导出为字符串。 |

### 评论

结构化文档标签 (SDT) 允许嵌入客户定义的语义及其 文档中的行为和外观。

在这个版本中，Aspose.Words 提供了许多公共方法和属性来 操纵T的行为和内容:Aspose.Words.Markup.StructuredDocumentTag。 将 SDT 节点映射到文档中的自定义 XML 包可以使用 [`XmlMapping`](./xmlmapping)财产。

[`StructuredDocumentTag`](../structureddocumenttag)可以出现在文档中的以下位置:

* 块级 - 在段落和表格中，作为[`Body`](../../aspose.words/body)的子级，[`HeaderFooter`](../../aspose.words/headerfooter), [`Comment`](../../aspose.words/comment),[`Footnote`](../../aspose.words.notes/footnote)或[`Shape`](../../aspose.words.drawing/shape)节点。
* 行级 - 在表中的行中，作为[`Table`](../../aspose.words.tables/table)节点的子节点。
* Cell-level - 在表格行中的单元格中，作为[`Row`](../../aspose.words.tables/row)节点的子节点.
* Inline-level - 在内部的内联内容中，作为[`Paragraph`](../../aspose.words/paragraph)的子级。
* 嵌套在另一个[`StructuredDocumentTag`](../structureddocumenttag)中。

### 例子

显示如何使用内容控制元素的样式。

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

* class [CompositeNode](../../aspose.words/compositenode)
* interface [IStructuredDocumentTag](../istructureddocumenttag)
* 命名空间 [Aspose.Words.Markup](../../aspose.words.markup)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
