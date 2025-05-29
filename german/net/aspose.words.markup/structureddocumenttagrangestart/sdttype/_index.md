---
title: StructuredDocumentTagRangeStart.SdtType
linktitle: SdtType
articleTitle: SdtType
second_title: Aspose.Words für .NET
description: Entdecken Sie die SdtType-Eigenschaft von StructuredDocumentTagRangeStart. Erfahren Sie, wie Sie strukturierte Dokument-Tag-Typen für ein verbessertes Dokumentenmanagement identifizieren.
type: docs
weight: 140
url: /de/net/aspose.words.markup/structureddocumenttagrangestart/sdttype/
---
## StructuredDocumentTagRangeStart.SdtType property

Ruft den Typ dieses strukturierten Dokument-Tags ab.

```csharp
public SdtType SdtType { get; }
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

* enum [SdtType](../../sdttype/)
* class [StructuredDocumentTagRangeStart](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
