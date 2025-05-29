---
title: StructuredDocumentTagRangeStart.RangeEnd
linktitle: RangeEnd
articleTitle: RangeEnd
second_title: Aspose.Words für .NET
description: Erkunden Sie die Eigenschaften StructuredDocumentTagRangeStart und RangeEnd, um Dokument-Tag-Grenzen zu definieren und so Ihr strukturiertes Dokumentmanagement zu verbessern.
type: docs
weight: 130
url: /de/net/aspose.words.markup/structureddocumenttagrangestart/rangeend/
---
## StructuredDocumentTagRangeStart.RangeEnd property

Gibt das Ende des Bereichs an, wenn der[`StructuredDocumentTag`](../../structureddocumenttag/) ist ein strukturiertes Dokument-Tag. Andernfalls wird zurückgegeben`null` .

```csharp
public StructuredDocumentTagRangeEnd RangeEnd { get; }
```

## Beispiele

Zeigt, wie die Eigenschaften von aus mehreren Abschnitten strukturierten Dokument-Tags abgerufen werden.

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

* class [StructuredDocumentTagRangeEnd](../../structureddocumenttagrangeend/)
* class [StructuredDocumentTagRangeStart](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
