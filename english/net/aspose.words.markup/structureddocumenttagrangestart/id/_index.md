---
title: StructuredDocumentTagRangeStart.Id
linktitle: Id
second_title: Aspose.Words for .NET API Reference
description: StructuredDocumentTagRangeStart Id property. Specifies a unique readonly persistent numerical Id for this structured document tag in C#.
type: docs
weight: 40
url: /net/aspose.words.markup/structureddocumenttagrangestart/id/
---
## StructuredDocumentTagRangeStart.Id property

Specifies a unique read-only persistent numerical Id for this structured document tag.

```csharp
public int Id { get; }
```

## Remarks

Id attribute shall follow these rules:

* The document shall retain structured document tag ids only if the whole document is cloned [`Clone`](../../../aspose.words/document/clone/).
* During [`ImportNode`](../../../aspose.words/documentbase/importnode/) Id shall be retained if import does not cause conflicts with other structured document tag Ids in the target document.
* If multiple structured document tag nodes specify the same decimal number value for the Id attribute, then the first structured document tag in the document shall maintain this original Id, and all subsequent structured document tag nodes shall have new identifiers assigned to them when the document is loaded.
* During standalone structured document tag INodeCloningListener) operation new unique ID will be generated for the cloned structured document tag node.
* If Id is not specified in the source document, then the structured document tag node shall have a new unique identifier assigned to it when the document is loaded.

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

* class [StructuredDocumentTagRangeStart](../)
* namespace [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* assembly [Aspose.Words](../../../)
