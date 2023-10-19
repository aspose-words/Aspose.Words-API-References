---
title: StructuredDocumentTagRangeStart.Id
linktitle: Id
articleTitle: Id
second_title: Aspose.Words for .NET
description: StructuredDocumentTagRangeStart Id mülk. Bu yapılandırılmış belge etiketi için benzersiz salt okunur kalıcı bir sayısal kimlik belirtir C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.markup/structureddocumenttagrangestart/id/
---
## StructuredDocumentTagRangeStart.Id property

Bu yapılandırılmış belge etiketi için benzersiz, salt okunur, kalıcı bir sayısal kimlik belirtir.

```csharp
public int Id { get; }
```

## Notlar

Kimlik özelliği şu kurallara uymalıdır:

* Belge, yalnızca document belgesinin tamamı kopyalandığında yapılandırılmış belge etiketi kimliklerini koruyacaktır[`Clone`](../../../aspose.words/document/clone/).
* Sırasında[`ImportNode`](../../../aspose.words/documentbase/importnode/) İçe aktarma, hedef belgedeki 'deki diğer yapılandırılmış belge etiketi kimlikleriyle çakışmaya neden olmazsa, kimliği korunacaktır.
* Birden fazla yapılandırılmış belge etiketi düğümü, Id özelliği için aynı ondalık sayı değerini belirtirse, , o zaman belgedeki ilk yapılandırılmış belge etiketi bu orijinal kimliği, koruyacak ve sonraki tüm yapılandırılmış belge etiketi düğümleri, aşağıdaki durumlarda kendilerine atanan yeni tanımlayıcılara sahip olacaktır: belge yüklendi.
* Bağımsız yapılandırılmış belge etiketi sırasındaINodeCloningListener)klonlanmış yapılandırılmış belge etiketi düğümü için yeni benzersiz kimlik işlemi be oluşturulacaktır.
* Kaynak belgede kimlik belirtilmemişse, yapılandırılmış belge etiket düğümüne, belge yüklendiğinde kendisine atanan yeni bir benzersiz tanımlayıcıya sahip olacaktır.

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
