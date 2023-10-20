---
title: StructuredDocumentTagRangeStart.Id
linktitle: Id
articleTitle: Id
second_title: Aspose.Words für .NET
description: StructuredDocumentTagRangeStart Id eigendom. Gibt eine eindeutige schreibgeschützte persistente numerische ID für dieses strukturierte DokumentTag an in C#.
type: docs
weight: 40
url: /de/net/aspose.words.markup/structureddocumenttagrangestart/id/
---
## StructuredDocumentTagRangeStart.Id property

Gibt eine eindeutige, schreibgeschützte, persistente numerische ID für dieses strukturierte Dokument-Tag an.

```csharp
public int Id { get; }
```

## Bemerkungen

Das ID-Attribut muss diesen Regeln folgen:

* Das Dokument behält strukturierte Dokument-Tag-IDs nur dann bei, wenn das gesamte document geklont wird[`Clone`](../../../aspose.words/document/clone/).
* Während[`ImportNode`](../../../aspose.words/documentbase/importnode/) Die -ID soll beibehalten werden, wenn der Import keine Konflikte mit anderen strukturierten Dokument-Tag-IDs im des Zieldokuments verursacht.
* Wenn mehrere Tag-Knoten eines strukturierten Dokuments denselben Dezimalzahlenwert für das ID-Attribut angeben, , behält das erste Tag des strukturierten Dokuments im Dokument diese ursprüngliche ID bei, , und allen nachfolgenden Tag-Knoten eines strukturierten Dokuments werden neue Bezeichner zugewiesen, wenn Das Dokument wird geladen.
* Während eines eigenständigen strukturierten Dokument-TagsINodeCloningListener)Für den geklonten Strukturdokument-Tag-Knoten wird eine neue eindeutige ID generiert.
* Wenn im Quelldokument keine ID angegeben ist, wird dem Tag-Knoten des strukturierten Dokuments beim Laden des Dokuments eine neue eindeutige Kennung zugewiesen .

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

* class [StructuredDocumentTagRangeStart](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
