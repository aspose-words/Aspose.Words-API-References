---
title: Class StructuredDocumentTagRangeStart
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Markup.StructuredDocumentTagRangeStart 班级. 代表一个开始 远程接受多部分内容的结构化文档标签 另请参阅StructuredDocumentTagRangeEnd.
type: docs
weight: 3850
url: /zh/net/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class

代表一个开始 **远程**接受多部分内容的结构化文档标签。 另请参阅[`StructuredDocumentTagRangeEnd`](../structureddocumenttagrangeend/).

```csharp
public class StructuredDocumentTagRangeStart : Node, IEnumerable<Node>, IStructuredDocumentTag
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [StructuredDocumentTagRangeStart](structureddocumenttagrangestart/)(DocumentBase, SdtType) | 初始化 **结构化文档标签范围开始**类. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [ChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/childnodes/) { get; } | 获取此范围开始节点和范围结束节点之间的所有节点。 |
| [Color](../../aspose.words.markup/structureddocumenttagrangestart/color/) { get; set; } | 获取或设置结构化文档标签的颜色。 |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取该节点所属的文档。 |
| [Id](../../aspose.words.markup/structureddocumenttagrangestart/id/) { get; } | 为此结构化文档标签指定一个唯一的只读持久数字 ID。 |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | 如果此节点可以包含其他节点，则返回 true。 |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttagrangestart/isshowingplaceholdertext/) { get; set; } | 指定此结构化文档标记的内容是否应解释为包含 占位符文本（与结构化文档标记中的常规文本内容相反）。 |
| [LastChild](../../aspose.words.markup/structureddocumenttagrangestart/lastchild/) { get; } | 获取 stdContent 范围内的最后一个孩子。 |
| [Level](../../aspose.words.markup/structureddocumenttagrangestart/level/) { get; } | 获取此结构化文档标记范围开始出现在文档树中的级别。 |
| [LockContentControl](../../aspose.words.markup/structureddocumenttagrangestart/lockcontentcontrol/) { get; set; } | 当设置为 true 时，此属性将禁止用户删除此结构化文档标签。 |
| [LockContents](../../aspose.words.markup/structureddocumenttagrangestart/lockcontents/) { get; set; } | 当设置为 true 时，此属性将禁止用户编辑此结构化文档标签的内容。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧跟此节点的节点。 |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangestart/nodetype/) { get; } |  |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [Placeholder](../../aspose.words.markup/structureddocumenttagrangestart/placeholder/) { get; } | 获取[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)包含当 此结构化文档标记运行内容为空时应显示的占位符文本，关联的映射XML元素为空，如指定 通过[`XmlMapping`](./xmlmapping/)元素或[`IsShowingPlaceholderText`](./isshowingplaceholdertext/)元素为真。 |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttagrangestart/placeholdername/) { get; set; } | 获取或设置名称[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)包含占位符文本。 |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取紧接在此节点之前的节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回一个 **范围**表示此节点中包含的文档部分的对象。 |
| [RangeEnd](../../aspose.words.markup/structureddocumenttagrangestart/rangeend/) { get; } | 如果 StructuredDocumentTag 是范围结构化文档标记，则指定范围结束。 否则返回null。 |
| [SdtType](../../aspose.words.markup/structureddocumenttagrangestart/sdttype/) { get; } | 获取此结构化文档标签的类型。 |
| [Tag](../../aspose.words.markup/structureddocumenttagrangestart/tag/) { get; set; } | 指定与当前结构化文档标签节点关联的标签。 不能为空。 |
| [Title](../../aspose.words.markup/structureddocumenttagrangestart/title/) { get; set; } | 指定与此结构化文档标签关联的友好名称。 不能为空。 |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxml/) { get; } | 获取一个字符串，该字符串表示包含在FlatOpc格式. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttagrangestart/xmlmapping/) { get; } | 获取一个对象，该对象表示此结构化文档标记范围到当前文档的自定义 XML 部分中的 XML 数据 的映射。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangestart/accept/)(DocumentVisitor) |  |
| [AppendChild](../../aspose.words.markup/structureddocumenttagrangestart/appendchild/)(Node) | 将指定节点添加到 stdContent 范围的末尾。 |
| [Clone](../../aspose.words/node/clone/)(bool) | 创建节点的副本。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | 获取指定的第一个祖先[`NodeType`](../../aspose.words/nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | 获取指定对象类型的第一个祖先。 |
| [GetChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/getchildnodes/)(NodeType, bool) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagrangestart/getenumerator/)() | 为在该节点的子节点上的每个样式迭代提供支持。 |
| virtual [GetText](../../aspose.words/node/gettext/)() | 获取该节点及其所有子节点的文本。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | 根据前序树遍历算法获取下一个节点。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | 根据前序树遍历算法获取上一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 从父级中移除自身。 |
| [RemoveAllChildren](../../aspose.words.markup/structureddocumenttagrangestart/removeallchildren/)() | 删除此范围开始节点和范围结束节点之间的所有节点。 |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttagrangestart/removeselfonly/)() | 删除结构化文档标记的此范围开始和适当范围结束节点， 但将其内容保留在文档树内。 |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | 使用指定的保存选项将节点的内容导出为字符串。 |

### 评论

可以是[`Body`](../../aspose.words/body/)节点 **只要**.

### 例子

显示如何获取多节结构化文档标签的属性。

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


