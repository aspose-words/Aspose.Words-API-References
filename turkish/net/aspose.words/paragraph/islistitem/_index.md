---
title: Paragraph.IsListItem
linktitle: IsListItem
articleTitle: IsListItem
second_title: Aspose.Words for .NET
description: Paragraph IsListItem mülk. Paragrafın orijinal revizyondaki madde işaretli veya numaralı listedeki bir öğe olması durumunda doğrudur C#'da.
type: docs
weight: 120
url: /tr/net/aspose.words/paragraph/islistitem/
---
## Paragraph.IsListItem property

Paragrafın orijinal revizyondaki madde işaretli veya numaralı listedeki bir öğe olması durumunda doğrudur.

```csharp
public bool IsListItem { get; }
```

## Örnekler

Bir listenin başka bir listenin içine nasıl yerleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Liste, paragraf kümelerini önek sembolleri ve girintilerle düzenlememize ve süslememize olanak tanır.
 // Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
 // Bir listeyi belge oluşturucunun "ListFormat" özelliğini kullanarak başlatabilir ve sonlandırabiliriz.
// Bir listenin başı ile sonu arasına eklediğimiz her paragraf, listede bir öğe haline gelecektir.
// Başlıklar için bir taslak listesi oluşturun.
List outlineList = doc.Lists.Add(ListTemplate.OutlineNumbers);
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 1");

// Numaralandırılmış bir liste oluşturun.
List numberedList = doc.Lists.Add(ListTemplate.NumberDefault);
builder.ListFormat.List = numberedList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Numbered list item 1.");

// Listeyi oluşturan her paragraf bu bayrağa sahip olacaktır.
Assert.True(builder.CurrentParagraph.IsListItem);
Assert.True(builder.ParagraphFormat.IsListItem);

// Madde işaretli bir liste oluşturun.
List bulletedList = doc.Lists.Add(ListTemplate.BulletDefault);
builder.ListFormat.List = bulletedList;
builder.ParagraphFormat.LeftIndent = 72;
builder.Writeln("Bulleted list item 1.");
builder.Writeln("Bulleted list item 2.");
builder.ParagraphFormat.ClearFormatting();

// Numaralandırılmış listeye geri dönelim.
builder.ListFormat.List = numberedList;
builder.Writeln("Numbered list item 2.");
builder.Writeln("Numbered list item 3.");

// Anahat listesine geri dönelim.
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 2");

builder.ParagraphFormat.ClearFormatting();

builder.Document.Save(ArtifactsDir + "Lists.NestedLists.docx");
```

### Ayrıca bakınız

* class [Paragraph](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
