---
title: DocumentBuilder.MoveToSection
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder yöntem. İmleci belirtilen bölümdeki gövdenin başlangıcına taşır.
type: docs
weight: 580
url: /tr/net/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder.MoveToSection method

İmleci belirtilen bölümdeki gövdenin başlangıcına taşır.

```csharp
public void MoveToSection(int sectionIndex)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| sectionIndex | Int32 | Taşınacak bölümün dizini. |

### Notlar

Ne zaman*sectionIndex* 0'dan büyük veya ona eşitse, belgenin başlangıcındaki from dizinini belirtir ve 0 ilk bölümdür. Ne zaman*sectionIndex* 0, 'den küçükse, belgenin sonundan -1 son bölüm olacak şekilde bir dizin belirtir.

İmleç metindeki ilk paragrafa taşınır.[`Body`](../../body/) belirtilen bölümün

### Örnekler

DocumentBuilder'ı kullanarak bir belgede üstbilgilerin ve altbilgilerin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İlk, çift ve tek sayfalar için farklı üstbilgi ve altbilgi istediğimizi belirtin.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Başlıkları oluşturun, ardından her başlık türünü görüntülemek için belgeye üç sayfa ekleyin.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

### Ayrıca bakınız

* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


