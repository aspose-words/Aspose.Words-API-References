---
title: StructuredDocumentTagRangeEnd.Id
linktitle: Id
articleTitle: Id
second_title: Aspose.Words für .NET
description: StructuredDocumentTagRangeEnd Id eigendom. Gibt hierfür eine eindeutige schreibgeschützte persistente numerische ID anStructuredDocumentTagRange node. EntsprechendStructuredDocumentTagRangeStart Knoten hat das gleicheId  in C#.
type: docs
weight: 20
url: /de/net/aspose.words.markup/structureddocumenttagrangeend/id/
---
## StructuredDocumentTagRangeEnd.Id property

Gibt hierfür eine eindeutige, schreibgeschützte, persistente numerische ID an**StructuredDocumentTagRange** node. Entsprechend[`StructuredDocumentTagRangeStart`](../../structureddocumenttagrangestart/) Knoten hat das gleiche[`Id`](../../structureddocumenttagrangestart/id/) .

```csharp
public int Id { get; }
```

## Beispiele

Zeigt, wie die Eigenschaften von strukturierten Dokument-Tags mit mehreren Abschnitten abgerufen werden.

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

### Siehe auch

* class [StructuredDocumentTagRangeEnd](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
