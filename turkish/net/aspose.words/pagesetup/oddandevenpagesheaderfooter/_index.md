---
title: PageSetup.OddAndEvenPagesHeaderFooter
linktitle: OddAndEvenPagesHeaderFooter
articleTitle: OddAndEvenPagesHeaderFooter
second_title: Aspose.Words for .NET
description: PageSetup OddAndEvenPagesHeaderFooter mülk. Belgenin tek sayılı ve çift sayılı sayfalar için farklı üstbilgileri ve altbilgileri varsa doğrudur C#'da.
type: docs
weight: 280
url: /tr/net/aspose.words/pagesetup/oddandevenpagesheaderfooter/
---
## PageSetup.OddAndEvenPagesHeaderFooter property

Belgenin tek sayılı ve çift sayılı sayfalar için farklı üstbilgileri ve altbilgileri varsa doğrudur.

```csharp
public bool OddAndEvenPagesHeaderFooter { get; set; }
```

## Notlar

Bu özelliğin değiştirilmesinin belgedeki tüm bölümleri etkileyeceğini unutmayın.

## Örnekler

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

Çift sayfa üstbilgilerinin/altbilgilerinin nasıl etkinleştirileceğini veya devre dışı bırakılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda iki tür üstbilgi/altbilgi bulunmaktadır.
// 1 - Bölümün her sayfasında görünen "Birincil" üstbilgi/altbilgi.
 // Birincil üstbilgi/altbilgiyi bir ilk ve çift sayfa üstbilgisi/altbilgisi ile geçersiz kılabiliriz.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Primary header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("Primary footer.");

// 2 - Bu bölümün her çift sayfasında görünen "Çift" üstbilgi/altbilgi.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Writeln("Even page header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterEven);
builder.Writeln("Even page footer.");

builder.MoveToSection(0);
builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Her bölümde sayfa görünümüyle ilgili özellikleri belirten bir "PageSetup" nesnesi bulunur
// yönlendirme, boyut ve kenarlıklar gibi.
// "OddAndEvenPagesHeaderFooter" özelliğini "true" olarak ayarlayın
// çift sayfa üstbilgisini/altbilgisini çift sayfalarda görüntülemek için.
// "OddAndEvenPagesHeaderFooter" özelliğini "false" olarak ayarlayın
// birincil üstbilgi/altbilgiyi çift sayfalarda görüntülemek için.
builder.PageSetup.OddAndEvenPagesHeaderFooter = oddAndEvenPagesHeaderFooter;

doc.Save(ArtifactsDir + "PageSetup.OddAndEvenPagesHeaderFooter.docx");
```

### Ayrıca bakınız

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
