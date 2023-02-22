---
title: StructuredDocumentTagRangeEnd.Id
second_title: Aspose.Words for .NET API Referansı
description: StructuredDocumentTagRangeEnd mülk. Bunun için benzersiz bir salt okunur kalıcı sayısal kimlik belirtir YapılandırılmışBelgeEtiketAralığı node. Karşılık gelenStructuredDocumentTagRangeStart düğüm aynıId .
type: docs
weight: 20
url: /tr/net/aspose.words.markup/structureddocumenttagrangeend/id/
---
## StructuredDocumentTagRangeEnd.Id property

Bunun için benzersiz bir salt okunur kalıcı sayısal kimlik belirtir **YapılandırılmışBelgeEtiketAralığı** node. Karşılık gelen[`StructuredDocumentTagRangeStart`](../../structureddocumenttagrangestart/) düğüm aynı[`Id`](../../structureddocumenttagrangestart/id/) .

```csharp
public int Id { get; }
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

* class [StructuredDocumentTagRangeEnd](../)
* ad alanı [Aspose.Words.Markup](../../structureddocumenttagrangeend/)
* toplantı [Aspose.Words](../../../)


