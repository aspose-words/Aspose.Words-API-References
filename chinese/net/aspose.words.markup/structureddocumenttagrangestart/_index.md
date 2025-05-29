---
title: StructuredDocumentTagRangeStart Class
linktitle: StructuredDocumentTagRangeStart
articleTitle: StructuredDocumentTagRangeStart
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Markup.StructuredDocumentTagRangeStart 类，实现结构化文档中的无缝多部分内容管理。
type: docs
weight: 4780
url: /zh/net/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class

表示**远程**接受多部分内容的结构化文档标签。 另请参阅[`StructuredDocumentTagRangeEnd`](../structureddocumenttagrangeend/).

要了解更多信息，请访问[结构化文档标签或内容控制](https://docs.aspose.com/words/net/working-with-content-control-sdt/)文档文章。

```csharp
public class StructuredDocumentTagRangeStart : Node, IEnumerable<Node>, IStructuredDocumentTag
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [StructuredDocumentTagRangeStart](structureddocumenttagrangestart/)(*[DocumentBase](../../aspose.words/documentbase/), [SdtType](../sdttype/)*) | 初始化**结构化文档标签范围开始**类. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttagrangestart/appearance/) { get; set; } | 获取或设置结构化文档标签的外观。 |
| [Color](../../aspose.words.markup/structureddocumenttagrangestart/color/) { get; set; } | 获取或设置结构化文档标签的颜色。 |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取此节点所属的文档。 |
| [Id](../../aspose.words.markup/structureddocumenttagrangestart/id/) { get; } | 为此结构化文档标签指定一个唯一的只读持久数字 ID。 |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | 返回`真的`如果此节点可以包含其他节点。 |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttagrangestart/isshowingplaceholdertext/) { get; set; } | 指定此结构化文档标签的内容是否应解释为包含 占位符文本（与结构化文档标签内的常规文本内容相反）。 |
| [LastChild](../../aspose.words.markup/structureddocumenttagrangestart/lastchild/) { get; } | 获取 stdContent 范围内的最后一个子项。 |
| [Level](../../aspose.words.markup/structureddocumenttagrangestart/level/) { get; } | 获取此结构化文档标签范围开始在文档树中出现的级别。 |
| [LockContentControl](../../aspose.words.markup/structureddocumenttagrangestart/lockcontentcontrol/) { get; set; } | 设置为`真的`，此属性将禁止用户删除此结构化文档标签。 |
| [LockContents](../../aspose.words.markup/structureddocumenttagrangestart/lockcontents/) { get; set; } | 设置为`真的` ，此属性将禁止用户编辑此结构化文档标签的内容。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随此节点之后的节点。 |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangestart/nodetype/) { get; } | 返回StructuredDocumentTagRangeStart. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [Placeholder](../../aspose.words.markup/structureddocumenttagrangestart/placeholder/) { get; } | 获取[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)包含应显示的占位符文本 当此结构化文档标签运行内容为空时，关联的映射 XML 元素为空，如通过指定 [`XmlMapping`](./xmlmapping/)元素或[`IsShowingPlaceholderText`](./isshowingplaceholdertext/)元素是`真的`. |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttagrangestart/placeholdername/) { get; set; } | 获取或设置[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)包含占位符文本。 |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取此节点前一个节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回[`Range`](../../aspose.words/range/)表示此节点中包含的文档部分的对象。 |
| [RangeEnd](../../aspose.words.markup/structureddocumenttagrangestart/rangeend/) { get; } | 指定范围结束，如果[`StructuredDocumentTag`](../structureddocumenttag/)是一个范围结构化文档标签。 否则返回`无效的`. |
| [SdtType](../../aspose.words.markup/structureddocumenttagrangestart/sdttype/) { get; } | 获取此结构化文档标签的类型。 |
| [Tag](../../aspose.words.markup/structureddocumenttagrangestart/tag/) { get; set; } | 指定与当前结构化文档标签节点关联的标签。 不能`无效的`. |
| [Title](../../aspose.words.markup/structureddocumenttagrangestart/title/) { get; set; } | 指定与此结构化文档标签关联的友好名称。 不能`无效的`. |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxml/) { get; } | 获取表示节点中包含的 XML 的字符串FlatOpc格式. |
| [WordOpenXMLMinimal](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxmlminimal/) { get; } | 获取表示节点中包含的 XML 的字符串FlatOpc格式. 与[`WordOpenXML`](./wordopenxml/)属性，此方法生成一个精简的文档，排除任何与内容无关的部分。 |
| [XmlMapping](../../aspose.words.markup/structureddocumenttagrangestart/xmlmapping/) { get; } | 获取一个对象，该对象表示此结构化文档标签范围到当前文档的自定义 XML 部分中的 XML 数据的映射。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangestart/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | 接受访客。 |
| [AppendChild](../../aspose.words.markup/structureddocumenttagrangestart/appendchild/)(*[Node](../../aspose.words/node/)*) | 将指定节点添加到 stdContent 范围的末尾。 |
| [Clone](../../aspose.words/node/clone/)(*bool*) | 创建节点的副本。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | 获取指定的第一个祖先[`NodeType`](../../aspose.words/nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | 获取指定对象类型的第一个祖先。 |
| [GetChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagrangestart/getenumerator/)() | 为该节点的子节点提供对每个样式迭代的支持。 |
| virtual [GetText](../../aspose.words/node/gettext/)() | 获取此节点及其所有子节点的文本。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | 根据前序树遍历算法获取下一个节点。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | 根据前序树遍历算法获取前一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 将自身从父级中移除。 |
| [RemoveAllChildren](../../aspose.words.markup/structureddocumenttagrangestart/removeallchildren/)() | 删除此范围起始节点和范围结束节点之间的所有节点。 |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttagrangestart/removeselfonly/)() | 删除结构化文档标签的此范围起始和适当范围结束节点， 但保留其内容在文档树内。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的保存选项将节点内容导出为字符串。 |

## 评论

可以是[`Body`](../../aspose.words/body/)节点**仅有的**.

## 例子

展示如何获取多节结构化文档标签的属性。

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

StructuredDocumentTagRangeStart rangeStartTag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeStart, true)[0] as StructuredDocumentTagRangeStart;
StructuredDocumentTagRangeEnd rangeEndTag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeEnd, true)[0] as StructuredDocumentTagRangeEnd;

Console.WriteLine("StructuredDocumentTagRangeStart values:");
Console.WriteLine($"\t|Id: {rangeStartTag.Id}");
Console.WriteLine($"\t|Title: {rangeStartTag.Title}");
Console.WriteLine($"\t|PlaceholderName: {rangeStartTag.PlaceholderName}");
Console.WriteLine($"\t|IsShowingPlaceholderText: {rangeStartTag.IsShowingPlaceholderText}");
Console.WriteLine($"\t|LockContentControl: {rangeStartTag.LockContentControl}");
Console.WriteLine($"\t|LockContents: {rangeStartTag.LockContents}");
Console.WriteLine($"\t|Level: {rangeStartTag.Level}");
Console.WriteLine($"\t|NodeType: {rangeStartTag.NodeType}");
Console.WriteLine($"\t|RangeEnd: {rangeStartTag.RangeEnd}");
Console.WriteLine($"\t|Color: {rangeStartTag.Color.ToArgb()}");
Console.WriteLine($"\t|SdtType: {rangeStartTag.SdtType}");
Console.WriteLine($"\t|FlatOpcContent: {rangeStartTag.WordOpenXML}");
Console.WriteLine($"\t|Tag: {rangeStartTag.Tag}\n");

Console.WriteLine("StructuredDocumentTagRangeEnd values:");
Console.WriteLine($"\t|Id: {rangeEndTag.Id}");
Console.WriteLine($"\t|NodeType: {rangeEndTag.NodeType}");
```

### 也可以看看

* class [Node](../../aspose.words/node/)
* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* 命名空间 [Aspose.Words.Markup](../../aspose.words.markup/)
* 部件 [Aspose.Words](../../)
