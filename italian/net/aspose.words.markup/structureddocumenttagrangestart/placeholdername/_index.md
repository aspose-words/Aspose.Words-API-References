---
title: StructuredDocumentTagRangeStart.PlaceholderName
second_title: Aspose.Words per .NET API Reference
description: StructuredDocumentTagRangeStart proprietà. Ottiene o imposta il nome diBuildingBlock contenente testo segnaposto.
type: docs
weight: 120
url: /it/net/aspose.words.markup/structureddocumenttagrangestart/placeholdername/
---
## StructuredDocumentTagRangeStart.PlaceholderName property

Ottiene o imposta il nome di[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/) contenente testo segnaposto.

[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/) con questo nome[`Name`](../../../aspose.words.buildingblocks/buildingblock/name/) deve essere presente in[`GlossaryDocument`](../../../aspose.words/document/glossarydocument/) altrimentiInvalidOperationException si verificherà.

```csharp
public string PlaceholderName { get; set; }
```

### Esempi

Mostra come ottenere le proprietà dei tag di documenti strutturati a più sezioni.

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

* class [StructuredDocumentTagRangeStart](../)
* spazio dei nomi [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* assemblea [Aspose.Words](../../../)


