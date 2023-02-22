---
title: StructuredDocumentTagRangeStart.PlaceholderName
second_title: Aspose.Words for .NET API Referansı
description: StructuredDocumentTagRangeStart mülk. Adını alır veya ayarlarBuildingBlock yer tutucu metni içeren.
type: docs
weight: 120
url: /tr/net/aspose.words.markup/structureddocumenttagrangestart/placeholdername/
---
## StructuredDocumentTagRangeStart.PlaceholderName property

Adını alır veya ayarlar[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/) yer tutucu metni içeren.

Bu ada sahip BuildingBlock[`Name`](../../../aspose.words.buildingblocks/buildingblock/name/) içinde mevcut olması gerekir[`GlossaryDocument`](../../../aspose.words/document/glossarydocument/) aksi haldeInvalidOperationException gerçekleşecek.

```csharp
public string PlaceholderName { get; set; }
```

### Örnekler

Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerinin nasıl alınacağını gösterir.

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

### Ayrıca bakınız

* class [StructuredDocumentTagRangeStart](../)
* ad alanı [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* toplantı [Aspose.Words](../../../)


