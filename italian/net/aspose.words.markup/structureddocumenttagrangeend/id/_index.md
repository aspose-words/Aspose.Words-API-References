---
title: StructuredDocumentTagRangeEnd.Id
linktitle: Id
articleTitle: Id
second_title: Aspose.Words per .NET
description: Scopri la proprietà StructuredDocumentTagRangeEnd Id, un identificatore univoco e di sola lettura per un tagging dei documenti fluido. Migliora la tua gestione dei documenti oggi stesso!
type: docs
weight: 20
url: /it/net/aspose.words.markup/structureddocumenttagrangeend/id/
---
## StructuredDocumentTagRangeEnd.Id property

Specifica un ID numerico persistente di sola lettura univoco per questo**Intervallo di tag di documenti strutturati** node. Corrispondente[`StructuredDocumentTagRangeStart`](../../structureddocumenttagrangestart/) il nodo ha lo stesso[`Id`](../../structureddocumenttagrangestart/id/) .

```csharp
public int Id { get; }
```

## Esempi

Mostra come ottenere le proprietà dei tag dei documenti strutturati multisezione.

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

### Guarda anche

* class [StructuredDocumentTagRangeEnd](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
