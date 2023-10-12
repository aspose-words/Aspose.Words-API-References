---
title: StructuredDocumentTagRangeStart.Id
second_title: Aspose.Words for .NET API 参考
description: StructuredDocumentTagRangeStart 财产. 为此结构化文档标记指定唯一的只读持久数字 ID
type: docs
weight: 40
url: /zh/net/aspose.words.markup/structureddocumenttagrangestart/id/
---
## StructuredDocumentTagRangeStart.Id property

为此结构化文档标记指定唯一的只读持久数字 ID。

```csharp
public int Id { get; }
```

### 评论

Id 属性应遵循以下规则：

* 仅当克隆整个 document 时，文档才应保留结构化文档标签 ID[`Clone`](../../../aspose.words/document/clone/)。
* 期间[`ImportNode`](../../../aspose.words/documentbase/importnode/)如果导入不会导致与 目标文档中的其他结构化文档标记 Id 发生冲突，则应保留 Id。
* 如果多个结构化文档标签节点为 Id 属性指定相同的十进制数值， ，则文档中的第一个结构化文档标签应保留此原始 Id， ，并且所有后续结构化文档标签节点应在以下情况下分配新的标识符：文档已加载。
* 在独立结构化文档标记期间INodeCloningListener)操作将为克隆的结构化文档标签节点生成新的唯一ID。
* 如果源文档中未指定 Id，则在加载文档时，结构化文档标记节点应分配一个新的唯一标识符 。

### 例子

演示如何获取多节结构化文档标签的属性。

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

* class [StructuredDocumentTagRangeStart](../)
* 命名空间 [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* 部件 [Aspose.Words](../../../)


