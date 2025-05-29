---
title: StructuredDocumentTagRangeStart.Tag
linktitle: Tag
articleTitle: Tag
second_title: .NET için Aspose.Words
description: Gelişmiş belge etiketleme için StructuredDocumentTagRangeStart özelliğini keşfedin. İş akışınızı kolaylaştırmak için etiketleri düğümlerle kolayca ilişkilendirin!
type: docs
weight: 150
url: /tr/net/aspose.words.markup/structureddocumenttagrangestart/tag/
---
## StructuredDocumentTagRangeStart.Tag property

Geçerli yapılandırılmış belge etiketi düğümüyle ilişkili bir etiketi belirtir. Olamaz`hükümsüz` .

```csharp
public string Tag { get; set; }
```

## Notlar

Bir etiket, uygulamaların görünür bir kullanıcı dostu ad sağlamadan tanımlamak için yapılandırılmış document etiketiyle ilişkilendirebileceği keyfi bir dizedir.

## Örnekler

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
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
