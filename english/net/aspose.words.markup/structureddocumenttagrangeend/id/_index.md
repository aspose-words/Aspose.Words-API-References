---
title: StructuredDocumentTagRangeEnd.Id
linktitle: Id
articleTitle: Id
second_title: Aspose.Words for .NET API Reference
description: StructuredDocumentTagRangeEnd Id property. Specifies a unique readonly persistent numerical Id for this StructuredDocumentTagRange node. Corresponding StructuredDocumentTagRangeStart node has the same Id in C#.
type: docs
weight: 20
url: /net/aspose.words.markup/structureddocumenttagrangeend/id/
---
## StructuredDocumentTagRangeEnd.Id property

Specifies a unique read-only persistent numerical Id for this **StructuredDocumentTagRange** node. Corresponding [`StructuredDocumentTagRangeStart`](../../structureddocumenttagrangestart/) node has the same [`Id`](../../structureddocumenttagrangestart/id/).

```csharp
public int Id { get; }
```

## Examples

Shows how to get the properties of multi-section structured document tags.

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

### See Also

* class [StructuredDocumentTagRangeEnd](../)
* namespace [Aspose.Words.Markup](../../structureddocumenttagrangeend/)
* assembly [Aspose.Words](../../../)
