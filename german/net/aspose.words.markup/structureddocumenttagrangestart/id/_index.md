---
title: StructuredDocumentTagRangeStart.Id
linktitle: Id
articleTitle: Id
second_title: Aspose.Words für .NET
description: Entdecken Sie die StructuredDocumentTagRangeStart Id-Eigenschaft – Ihren Schlüssel zu einer eindeutigen, schreibgeschützten numerischen Kennung für effizientes Dokument-Tagging.
type: docs
weight: 40
url: /de/net/aspose.words.markup/structureddocumenttagrangestart/id/
---
## StructuredDocumentTagRangeStart.Id property

Gibt eine eindeutige, schreibgeschützte, dauerhafte numerische ID für dieses strukturierte Dokument-Tag an.

```csharp
public int Id { get; }
```

## Bemerkungen

Das ID-Attribut muss diesen Regeln folgen:

* Das Dokument soll strukturierte Dokument-Tag-IDs nur dann behalten, wenn das gesamte Dokument geklont wird[`Clone`](../../../aspose.words/document/clone/).
* Während[`ImportNode`](../../../aspose.words/documentbase/importnode/) Die ID muss beibehalten werden, wenn der Import keine Konflikte mit anderen strukturierten Dokument-Tag-IDs im Zieldokument verursacht.
* Wenn mehrere strukturierte Dokument-Tag-Knoten denselben Dezimalwert für das ID-Attribut angeben, dann muss der erste strukturierte Dokument-Tag im Dokument diese ursprüngliche ID beibehalten, und allen nachfolgenden strukturierten Dokument-Tag-Knoten müssen beim Laden des Dokuments neue Kennungen zugewiesen werden.
* Während des eigenständigen strukturierten DokumenttagsINodeCloningListener) Bei der Operation wird für den geklonten strukturierten Dokument-Tag-Knoten eine neue eindeutige ID generiert.
* Wenn im Quelldokument keine ID angegeben ist, muss dem Tag-Knoten des strukturierten Dokuments beim Laden des Dokuments eine neue eindeutige Kennung zugewiesen werden.

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

* class [StructuredDocumentTagRangeStart](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
