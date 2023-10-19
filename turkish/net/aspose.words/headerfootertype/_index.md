---
title: HeaderFooterType Enum
linktitle: HeaderFooterType
articleTitle: HeaderFooterType
second_title: Aspose.Words for .NET
description: Aspose.Words.HeaderFooterType Sıralama. Word dosyasında bulunan üstbilgi veya altbilginin türünü tanımlar C#'da.
type: docs
weight: 3120
url: /tr/net/aspose.words/headerfootertype/
---
## HeaderFooterType enumeration

Word dosyasında bulunan üstbilgi veya altbilginin türünü tanımlar.

```csharp
public enum HeaderFooterType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| HeaderEven | `0` | Çift sayılı sayfalar için başlık. |
| HeaderPrimary | `1` | Birincil başlık, tek sayılı sayfalar için de kullanılır. |
| FooterEven | `2` | Çift sayılı sayfalar için altbilgi. |
| FooterPrimary | `3` | Birincil altbilgi, tek sayılı sayfalar için de kullanılır. |
| HeaderFirst | `4` | Bölümün ilk sayfasının başlığı. |
| FooterFirst | `5` | Bölümün ilk sayfası için alt bilgi. |

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

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
