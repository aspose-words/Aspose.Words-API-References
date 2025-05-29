---
title: StructuredDocumentTag Class
linktitle: StructuredDocumentTag
articleTitle: StructuredDocumentTag
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Markup.StructuredDocumentTag 类，高效控制文档内容。使用 SDT 功能增强您的文档管理！
type: docs
weight: 4750
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
| [StructuredDocumentTag](structureddocumenttag/)(*[DocumentBase](../../aspose.words/documentbase/), [SdtType](../sdttype/), [MarkupLevel](../markuplevel/)*) | 初始化**结构化文档标签**类. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttag/appearance/) { get; set; } | 获取/设置结构化文档标签的外观。 |
| [BuildingBlockCategory](../../aspose.words.markup/structureddocumenttag/buildingblockcategory/) { get; set; } | 指定此构建块的类别**特殊和差别待遇**node. 不能`无效的`. |
| [BuildingBlockGallery](../../aspose.words.markup/structureddocumenttag/buildingblockgallery/) { get; set; } | 指定此构建块的类型**特殊和差别待遇**. 不能`无效的`. |
| [CalendarType](../../aspose.words.markup/structureddocumenttag/calendartype/) { get; set; } | 指定此日历的类型**特殊和差别待遇**. 默认为Default |
| [Checked](../../aspose.words.markup/structureddocumenttag/checked/) { get; set; } | 获取/设置复选框的当前状态**特殊和差别待遇**. 此属性的默认值为`错误的`. |
| [Color](../../aspose.words.markup/structureddocumenttag/color/) { get; set; } | 获取或设置结构化文档标签的颜色。 |
| [ContentsFont](../../aspose.words.markup/structureddocumenttag/contentsfont/) { get; } | 将应用于输入文本的字体格式**特殊和差别待遇**. |
| [Count](../../aspose.words/compositenode/count/) { get; } | 获取此节点的直属子节点的数量。 |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| [DateDisplayFormat](../../aspose.words.markup/structureddocumenttag/datedisplayformat/) { get; set; } | 表示日期显示格式的字符串。 |
| [DateDisplayLocale](../../aspose.words.markup/structureddocumenttag/datedisplaylocale/) { get; set; } | 允许设置/获取此处显示的日期的语言格式**特殊和差别待遇**. |
| [DateStorageFormat](../../aspose.words.markup/structureddocumenttag/datestorageformat/) { get; set; } | 获取/设置日期 SDT 的日期存储格式**特殊和差别待遇**绑定到文档数据存储中的 XML 节点。 默认值为DateTime |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取此节点所属的文档。 |
| [EndCharacterFont](../../aspose.words.markup/structureddocumenttag/endcharacterfont/) { get; } | 将应用于输入文本的最后一个字符的字体格式**特殊和差别待遇**. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | 获取节点的第一个子节点。 |
| [FullDate](../../aspose.words.markup/structureddocumenttag/fulldate/) { get; set; } | 指定上次输入此的完整日期和时间**特殊和差别待遇**. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | 返回`真的`如果此节点有任何子节点。 |
| [Id](../../aspose.words.markup/structureddocumenttag/id/) { get; } | 指定一个唯一的只读持久数字 ID**特殊和差别待遇**。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | 返回`真的`因为这个节点可以有子节点。 |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttag/isshowingplaceholdertext/) { get; set; } | 指定此内容是否**特殊和差别待遇**应解释为包含占位符文本 （与 SDT 中的常规文本内容相反）。 |
| [IsTemporary](../../aspose.words.markup/structureddocumenttag/istemporary/) { get; set; } | 指定此**特殊和差别待遇**当其内容被修改时，应从 WordProcessingML 文档中删除。 |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | 获取节点的最后一个子节点。 |
| [Level](../../aspose.words.markup/structureddocumenttag/level/) { get; } | 获取此**特殊和差别待遇**出现在文档树中。 |
| [ListItems](../../aspose.words.markup/structureddocumenttag/listitems/) { get; } | 获取[`SdtListItemCollection`](../sdtlistitemcollection/)与此相关**特殊和差别待遇**. |
| [LockContentControl](../../aspose.words.markup/structureddocumenttag/lockcontentcontrol/) { get; set; } | 设置为`真的` ，此属性将禁止用户删除此**特殊和差别待遇**. |
| [LockContents](../../aspose.words.markup/structureddocumenttag/lockcontents/) { get; set; } | 设置为`真的` ，此属性将禁止用户编辑此**特殊和差别待遇**. |
| [Multiline](../../aspose.words.markup/structureddocumenttag/multiline/) { get; set; } | 指定此**特殊和差别待遇**允许多行文本。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随此节点之后的节点。 |
| override [NodeType](../../aspose.words.markup/structureddocumenttag/nodetype/) { get; } | 返回StructuredDocumentTag. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [Placeholder](../../aspose.words.markup/structureddocumenttag/placeholder/) { get; } | 获取[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)包含当此 SDT 运行内容为空时应显示的占位符文本， 关联的映射 XML 元素为空，如通过[`XmlMapping`](./xmlmapping/)element 或[`IsShowingPlaceholderText`](./isshowingplaceholdertext/)元素是`真的`. |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttag/placeholdername/) { get; set; } | 获取或设置[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)包含占位符文本。 |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取此节点前一个节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回[`Range`](../../aspose.words/range/)表示此节点中包含的文档部分的对象。 |
| [SdtType](../../aspose.words.markup/structureddocumenttag/sdttype/) { get; } | 获取此类型**结构化文档标签**. |
| [Style](../../aspose.words.markup/structureddocumenttag/style/) { get; set; } | 获取或设置结构化文档标签的样式。 |
| [StyleName](../../aspose.words.markup/structureddocumenttag/stylename/) { get; set; } | 获取或设置应用于结构化文档标签的样式的名称。 |
| [Tag](../../aspose.words.markup/structureddocumenttag/tag/) { get; set; } | 指定与当前 SDT 节点关联的标签。 不能`无效的`. |
| [Title](../../aspose.words.markup/structureddocumenttag/title/) { get; set; } | 指定与此相关的友好名称**特殊和差别待遇**. 不能`无效的`. |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttag/wordopenxml/) { get; } | 获取表示节点中包含的 XML 的字符串FlatOpc格式. |
| [WordOpenXMLMinimal](../../aspose.words.markup/structureddocumenttag/wordopenxmlminimal/) { get; } | 获取表示节点中包含的 XML 的字符串FlatOpc格式. 与[`WordOpenXML`](./wordopenxml/)属性，此方法生成一个精简的文档，排除任何与内容无关的部分。 |
| [XmlMapping](../../aspose.words.markup/structureddocumenttag/xmlmapping/) { get; } | 获取一个对象，该对象表示此结构化文档标签到当前文档的自定义 XML 部分中的 XML 数据的映射。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttag/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | 接受访客。 |
| override [AcceptEnd](../../aspose.words.markup/structureddocumenttag/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | 接受访问者访问 StructuredDocumentTag 的末尾。 |
| override [AcceptStart](../../aspose.words.markup/structureddocumenttag/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | 接受访问者访问 StructuredDocumentTag 的开头。 |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [Clear](../../aspose.words.markup/structureddocumenttag/clear/)() | 清除此结构化文档标签的内容，并显示占位符（如果已定义）。 |
| [Clone](../../aspose.words/node/clone/)(*bool*) | 创建节点的副本。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | 创建可用于遍历和读取节点的导航器。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | 获取指定的第一个祖先[`NodeType`](../../aspose.words/nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | 获取指定对象类型的第一个祖先。 |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | 返回与指定类型匹配的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | 为该节点的子节点提供对每个样式迭代的支持。 |
| override [GetText](../../aspose.words/compositenode/gettext/)() | 获取此节点及其所有子节点的文本。 |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | 返回子节点数组中指定子节点的索引。 |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | 在指定的参考节点后立即插入指定的节点。 |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | 在指定的参考节点之前立即插入指定的节点。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | 根据前序树遍历算法获取下一个节点。 |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | 将指定节点添加到此节点的子节点列表的开头。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | 根据前序树遍历算法获取前一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 将自身从父级中移除。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | 删除当前节点的所有子节点。 |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | 删除指定的子节点。 |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttag/removeselfonly/)() | 仅删除此 SDT 节点本身，但保留其在文档树中的内容。 |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | 删除所有[`SmartTag`](../smarttag/)当前节点的后代节点。 |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | 选择与 XPath 表达式匹配的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | 选择第一个[`Node`](../../aspose.words/node/)与 XPath 表达式匹配。 |
| [SetCheckedSymbol](../../aspose.words.markup/structureddocumenttag/setcheckedsymbol/)(*int, string*) | 设置用于表示复选框内容控件的选中状态的符号。 |
| [SetUncheckedSymbol](../../aspose.words.markup/structureddocumenttag/setuncheckedsymbol/)(*int, string*) | 设置用于表示复选框内容控件未选中状态的符号。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的保存选项将节点内容导出为字符串。 |

## 评论

结构化文档标签 (SDT) 允许将客户定义的语义及其行为和外观嵌入到文档中。

在此版本中，Aspose.Words 提供了许多公共方法和属性来操纵`StructuredDocumentTag`. 可以使用 将 SDT 节点映射到文档中的自定义 XML 包[`XmlMapping`](./xmlmapping/)财产。

`StructuredDocumentTag`可以出现在文档中的以下位置：

* 块级 - 在段落和表格中，作为[`Body`](../../aspose.words/body/)，[`HeaderFooter`](../../aspose.words/headerfooter/), [`Comment`](../../aspose.words/comment/)，[`Footnote`](../../aspose.words.notes/footnote/)或[`Shape`](../../aspose.words.drawing/shape/)节点。
* 行级 - 在表格的行中，作为[`Table`](../../aspose.words.tables/table/)节点。
* 单元格级别 - 在表格行的单元格中，作为[`Row`](../../aspose.words.tables/row/)节点。
* 内联级别 - 在内联内容中，作为[`Paragraph`](../../aspose.words/paragraph/)。
* 嵌套在另一个中`StructuredDocumentTag`。

## 例子

展示如何使用内容控制元素的样式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 以下是将文档中的样式应用到结构化文档标签的两种方法。
// 1 - 从文档的样式集合中应用样式对象：
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - 通过名称引用文档中的样式：
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
