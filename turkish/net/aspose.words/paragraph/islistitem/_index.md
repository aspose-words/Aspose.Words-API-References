---
title: Paragraph.IsListItem
linktitle: IsListItem
articleTitle: IsListItem
second_title: .NET için Aspose.Words
description: Bir paragrafın orijinal revizyonunda madde işaretli veya numaralı bir listenin parçası olup olmadığını belirten Paragraph IsListItem özelliğini keşfedin. Belgenizin yapısını geliştirin!
type: docs
weight: 120
url: /tr/net/aspose.words/paragraph/islistitem/
---
## Paragraph.IsListItem property

Paragraf orijinal revizyonda madde işaretli veya numaralı bir listede yer aldığında doğrudur.

```csharp
public bool IsListItem { get; }
```

## Örnekler

Bir listenin başka bir listenin içine nasıl yerleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir liste, paragraf kümelerini önek sembolleri ve girintilerle düzenlememize ve süslememize olanak tanır.
 // Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
 // Bir listeyi, bir belge oluşturucunun "ListFormat" özelliğini kullanarak başlatabilir ve sonlandırabiliriz.
// Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf listede bir öğe haline gelecektir.
// Başlıklar için bir ana hat listesi oluşturun.
List outlineList = doc.Lists.Add(ListTemplate.OutlineNumbers);
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 1");

// Numaralandırılmış bir liste oluştur.
List numberedList = doc.Lists.Add(ListTemplate.NumberDefault);
builder.ListFormat.List = numberedList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Numbered list item 1.");

// Liste oluşturan her paragraf bu bayrağa sahip olacaktır.
Assert.True(builder.CurrentParagraph.IsListItem);
Assert.True(builder.ParagraphFormat.IsListItem);

// Madde işaretli bir liste oluşturun.
List bulletedList = doc.Lists.Add(ListTemplate.BulletDefault);
builder.ListFormat.List = bulletedList;
builder.ParagraphFormat.LeftIndent = 72;
builder.Writeln("Bulleted list item 1.");
builder.Writeln("Bulleted list item 2.");
builder.ParagraphFormat.ClearFormatting();

// Numaralandırılmış listeye geri dön.
builder.ListFormat.List = numberedList;
builder.Writeln("Numbered list item 2.");
builder.Writeln("Numbered list item 3.");

// Anahat listesine geri dön.
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
