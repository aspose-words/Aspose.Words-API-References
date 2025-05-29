---
title: StructuredDocumentTagRangeStart.Tag
linktitle: Tag
articleTitle: Tag
second_title: Aspose.Words för .NET
description: Upptäck egenskapen StructuredDocumentTagRangeStart för förbättrad dokumenttaggning. Koppla enkelt taggar med noder för att effektivisera ditt arbetsflöde!
type: docs
weight: 150
url: /sv/net/aspose.words.markup/structureddocumenttagrangestart/tag/
---
## StructuredDocumentTagRangeStart.Tag property

Anger en tagg som är associerad med den aktuella noden för strukturerat dokumenttagg. Kan inte`null` .

```csharp
public string Tag { get; set; }
```

## Anmärkningar

En tagg är en godtycklig sträng som program kan associera med den strukturerade document -taggen för att identifiera den utan att ange ett synligt vänligt namn.

## Exempel

Visar hur man hämtar egenskaperna för taggar för strukturerade dokument med flera sektioner.

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

### Se även

* class [StructuredDocumentTagRangeStart](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
