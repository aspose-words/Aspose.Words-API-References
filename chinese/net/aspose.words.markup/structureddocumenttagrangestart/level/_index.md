---
title: StructuredDocumentTagRangeStart.Level
second_title: Aspose.Words for .NET API 参考
description: StructuredDocumentTagRangeStart 财产. 获取此结构化文档标记范围开始出现在文档树中的级别
type: docs
weight: 70
url: /zh/net/aspose.words.markup/structureddocumenttagrangestart/level/
---
## StructuredDocumentTagRangeStart.Level property

获取此结构化文档标记范围开始出现在文档树中的级别。

```csharp
public MarkupLevel Level { get; }
```

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

* enum [MarkupLevel](../../markuplevel/)
* class [StructuredDocumentTagRangeStart](../)
* 命名空间 [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* 部件 [Aspose.Words](../../../)


