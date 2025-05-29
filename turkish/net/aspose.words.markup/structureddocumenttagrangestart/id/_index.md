---
title: StructuredDocumentTagRangeStart.Id
linktitle: Id
articleTitle: Id
second_title: .NET için Aspose.Words
description: Verimli belge etiketleme için benzersiz, salt okunur sayısal tanımlayıcıya giden anahtarınız olan StructuredDocumentTagRangeStart Id özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.markup/structureddocumenttagrangestart/id/
---
## StructuredDocumentTagRangeStart.Id property

Bu yapılandırılmış belge etiketi için benzersiz, salt okunur, kalıcı bir sayısal Kimlik belirtir.

```csharp
public int Id { get; }
```

## Notlar

Kimlik niteliği şu kurallara uymalıdır:

* Belge, yalnızca tüm document klonlandığında yapılandırılmış belge etiketi kimliklerini koruyacaktır[`Clone`](../../../aspose.words/document/clone/).
* Sırasında[`ImportNode`](../../../aspose.words/documentbase/importnode/) Hedef belgedeki diğer yapılandırılmış belge etiketi kimlikleriyle çakışmalara neden olmazsa, kimliği korunmalıdır.
* Birden fazla yapılandırılmış belge etiketi düğümü, Id niteliği için aynı ondalık sayı değerini belirtiyorsa, belgedeki ilk yapılandırılmış belge etiketi bu orijinal Id'yi, koruyacak ve belge yüklendiğinde tüm sonraki yapılandırılmış belge etiketi düğümlerine yeni tanımlayıcılar atanacaktır.
* Bağımsız yapılandırılmış belge etiketi sırasındaINodeCloningListener) Klonlanmış yapılandırılmış belge etiketi düğümü için yeni benzersiz kimlik be oluşturulacaktır.
* Kaynak belgede Id belirtilmemişse, yapılandırılmış belge etiketi düğümü, belge yüklendiğinde kendisine atanmış yeni bir benzersiz tanımlayıcıya sahip olacaktır.

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
