---
title: Class StructuredDocumentTag
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Markup.StructuredDocumentTag 班级. 表示文档中的结构化文档标签SDT 或内容控制
type: docs
weight: 4060
url: /zh/net/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class

表示文档中的结构化文档标签（SDT 或内容控制）。

要了解更多信息，请访问[结构化文档标签或内容控制](https://docs.aspose.com/words/net/working-with-content-control-sdt/)文档文章。

```csharp
public class StructuredDocumentTag : CompositeNode, IStructuredDocumentTag
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [StructuredDocumentTag](structureddocumenttag/)(DocumentBase, SdtType, MarkupLevel) | 初始化一个新实例 **结构化文档标签**类. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttag/appearance/) { get; set; } | 获取/设置结构化文档标签的外观。 |
| [BuildingBlockCategory](../../aspose.words.markup/structureddocumenttag/buildingblockcategory/) { get; set; } | 指定此构建块的类别 **特殊测试**节点. 不能`无效的`. |
| [BuildingBlockGallery](../../aspose.words.markup/structureddocumenttag/buildingblockgallery/) { get; set; } | 指定构建块的类型 **特殊测试**. 不能`无效的`. |
| [CalendarType](../../aspose.words.markup/structureddocumenttag/calendartype/) { get; set; } | 指定此日历的类型 **特殊测试**. 默认为Default |
| [Checked](../../aspose.words.markup/structureddocumenttag/checked/) { get; set; } | 获取/设置复选框的当前状态 **特殊测试**. 此属性的默认值为`错误的`. |
| [Color](../../aspose.words.markup/structureddocumenttag/color/) { get; set; } | 获取或设置结构化文档标签的颜色。 |
| [ContentsFont](../../aspose.words.markup/structureddocumenttag/contentsfont/) { get; } | 将应用于输入文本的字体格式 **特殊测试**. |
| [Count](../../aspose.words/compositenode/count/) { get; } | 获取此节点的直接子节点的数量。 |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| [DateDisplayFormat](../../aspose.words.markup/structureddocumenttag/datedisplayformat/) { get; set; } | 表示日期显示格式的字符串。 不能`无效的`. 英语（美国）的日期为“mm/dd/yyyy” |
| [DateDisplayLocale](../../aspose.words.markup/structureddocumenttag/datedisplaylocale/) { get; set; } | 允许设置/获取在此显示的日期的语言格式 **特殊测试**. |
| [DateStorageFormat](../../aspose.words.markup/structureddocumenttag/datestorageformat/) { get; set; } | 获取/设置日期 SDT 的日期存储格式 **特殊测试**绑定到文档数据存储中的 XML 节点。 默认值为DateTime |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取该节点所属的文档。 |
| [EndCharacterFont](../../aspose.words.markup/structureddocumenttag/endcharacterfont/) { get; } | 将应用于输入文本的最后一个字符的字体格式 **特殊测试**. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | 获取节点的第一个子节点。 |
| [FullDate](../../aspose.words.markup/structureddocumenttag/fulldate/) { get; set; } | 指定上次输入此内容的完整日期和时间 **特殊测试**. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | 返回`真的`如果该节点有任何子节点. |
| [Id](../../aspose.words.markup/structureddocumenttag/id/) { get; } | 为此指定一个唯一的只读持久数字 ID **特殊测试**。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | 返回`真的`因为该节点可以有子节点。 |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttag/isshowingplaceholdertext/) { get; set; } | 指定此内容是否 **特殊测试**应被解释为包含占位符文本 （与 SDT 中的常规文本内容相反）。 |
| [IsTemporary](../../aspose.words.markup/structureddocumenttag/istemporary/) { get; set; } | 指定是否 **特殊测试**当其内容 被修改时，应从WordProcessingML文档中删除。 |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | 获取节点的最后一个子节点。 |
| [Level](../../aspose.words.markup/structureddocumenttag/level/) { get; } | 获取此级别 **特殊测试**出现在文档树中。 |
| [ListItems](../../aspose.words.markup/structureddocumenttag/listitems/) { get; } | 获取[`SdtListItemCollection`](../sdtlistitemcollection/)与此相关的 **特殊测试**. |
| [LockContentControl](../../aspose.words.markup/structureddocumenttag/lockcontentcontrol/) { get; set; } | 当设置为`真的` ，此属性将禁止用户删除此 **特殊测试**. |
| [LockContents](../../aspose.words.markup/structureddocumenttag/lockcontents/) { get; set; } | 当设置为`真的` ，此属性将禁止用户编辑此内容 **特殊测试**. |
| [Multiline](../../aspose.words.markup/structureddocumenttag/multiline/) { get; set; } | 指定是否 **特殊测试**允许多行文本。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随该节点的下一个节点。 |
| override [NodeType](../../aspose.words.markup/structureddocumenttag/nodetype/) { get; } | 返回StructuredDocumentTag. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [Placeholder](../../aspose.words.markup/structureddocumenttag/placeholder/) { get; } | 获取[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)包含当此 SDT 运行内容为空时应显示的占位符文本， 关联的映射 XML 元素为空，如通过[`XmlMapping`](./xmlmapping/)element 或[`IsShowingPlaceholderText`](./isshowingplaceholdertext/)元素是`真的`. |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttag/placeholdername/) { get; set; } | 获取或设置名称[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)包含占位符文本。 |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取紧邻此节点之前的节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回一个[`Range`](../../aspose.words/range/)表示此节点中包含的文档部分的对象。 |
| [SdtType](../../aspose.words.markup/structureddocumenttag/sdttype/) { get; } | 获取此类型 **结构化文档标签**. |
| [Style](../../aspose.words.markup/structureddocumenttag/style/) { get; set; } | 获取或设置结构化文档标签的样式。 |
| [StyleName](../../aspose.words.markup/structureddocumenttag/stylename/) { get; set; } | 获取或设置应用于结构化文档标记的样式名称。 |
| [Tag](../../aspose.words.markup/structureddocumenttag/tag/) { get; set; } | 指定与当前 SDT 节点关联的标记。 不能`无效的`. |
| [Title](../../aspose.words.markup/structureddocumenttag/title/) { get; set; } | 指定与此关联的友好名称 **特殊测试**. 不能`无效的`. |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttag/wordopenxml/) { get; } | 获取表示节点中包含的 XML 的字符串FlatOpc格式. |
| [WordOpenXMLMinimal](../../aspose.words.markup/structureddocumenttag/wordopenxmlminimal/) { get; } | 获取表示节点中包含的 XML 的字符串FlatOpc格式. 与[`WordOpenXML`](./wordopenxml/)属性，此方法生成一个精简文档，排除任何与内容无关的部分。 |
| [XmlMapping](../../aspose.words.markup/structureddocumenttag/xmlmapping/) { get; } | 获取一个对象，该对象表示此结构化文档标记到当前文档的自定义 XML 部分中的 XML 数据 的映射。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttag/accept/)(DocumentVisitor) | 接受访客。 |
| override [AcceptEnd](../../aspose.words.markup/structureddocumenttag/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words.markup/structureddocumenttag/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clear](../../aspose.words.markup/structureddocumenttag/clear/)() | 清除此结构化文档标记的内容并显示占位符（如果已定义）。 |
| [Clone](../../aspose.words/node/clone/)(bool) | 创建节点的副本。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | 创建可用于遍历和读取节点的导航器。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | 获取指定的第一个祖先[`NodeType`](../../aspose.words/nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | 获取指定对象类型的第一个祖先。 |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | 返回与指定类型匹配的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | 为该节点的子节点上的每个样式迭代提供支持。 |
| override [GetText](../../aspose.words/compositenode/gettext/)() | 获取此节点及其所有子节点的文本。 |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | 返回子节点数组中指定子节点的索引。 |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | 根据先序树遍历算法获取下一个节点。 |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | 根据先序树遍历算法获取前一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 将自身从父级中删除。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | 删除当前节点的所有子节点。 |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttag/removeselfonly/)() | 仅删除此 SDT 节点本身，但将其内容保留在文档树中。 |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | 删除所有[`SmartTag`](../smarttag/)当前节点的后代节点. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | 选择与 XPath 表达式匹配的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | 选择第一个[`Node`](../../aspose.words/node/)与 XPath 表达式匹配。 |
| [SetCheckedSymbol](../../aspose.words.markup/structureddocumenttag/setcheckedsymbol/)(int, string) | 设置用于表示复选框内容控件的选中状态的符号。 |
| [SetUncheckedSymbol](../../aspose.words.markup/structureddocumenttag/setuncheckedsymbol/)(int, string) | 设置用于表示复选框内容控件的未选中状态的符号。 |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | 使用指定的保存选项将节点的内容导出到字符串中。 |

### 评论

结构化文档标签 (SDT) 允许将客户定义的语义及其 行为和外观嵌入到文档中。

在此版本中，Aspose.Words 提供了许多公共方法和属性来操作 的行为和内容`StructuredDocumentTag`. 将 SDT 节点映射到文档中的自定义 XML 包可以使用 using 执行[`XmlMapping`](./xmlmapping/)财产。

`StructuredDocumentTag`可能出现在文档中的以下位置：

* 块级 - 在段落和表格中，作为[`Body`](../../aspose.words/body/),[`HeaderFooter`](../../aspose.words/headerfooter/), [`Comment`](../../aspose.words/comment/),[`Footnote`](../../aspose.words.notes/footnote/)或一个[`Shape`](../../aspose.words.drawing/shape/)节点。
* 行级 - 在表中的行中，作为[`Table`](../../aspose.words.tables/table/)节点。
* 单元格级 - 在表格行的单元格中，作为[`Row`](../../aspose.words.tables/row/)节点。
* 内联级别 - 在内部的内联内容中，作为 a 的子级[`Paragraph`](../../aspose.words/paragraph/)。
* 嵌套在另一个里面`StructuredDocumentTag`。

### 例子

展示如何使用内容控制元素的样式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 下面是将文档样式应用到结构化文档标签的两种方法。
// 1 - 从文档的样式集合中应用样式对象：
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

    Console.WriteLine(sdt.WordOpenXMLMinimal);

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### 也可以看看

* class [CompositeNode](../../aspose.words/compositenode/)
* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* 命名空间 [Aspose.Words.Markup](../../aspose.words.markup/)
* 部件 [Aspose.Words](../../)


