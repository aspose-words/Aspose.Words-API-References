---
title: SheetsPerBooklet
second_title: Aspose.Words for .NET API Referansı
description: Her kitapçığa dahil edilecek sayfa sayısını döndürür veya ayarlar.
type: docs
weight: 390
url: /tr/net/aspose.words/pagesetup/sheetsperbooklet/
---
## PageSetup.SheetsPerBooklet property

Her kitapçığa dahil edilecek sayfa sayısını döndürür veya ayarlar.

```csharp
public int SheetsPerBooklet { get; set; }
```

### Örnekler

Kitap katlama olarak yazdırılabilen bir belgenin nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();

// 16 sayfaya yayılan metin ekleyin.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Belgeyi kitap katlama biçiminde yazdırmak için ilk bölümün "PageSetup" özelliğini yapılandırın.
// Bu belgeyi her iki tarafa yazdırdığımızda, sayfaları istiflemek için alabiliriz
// ve hepsini bir kerede ortadan katlayın. Belgenin içeriği bir kitap katlaması şeklinde sıralanacaktır.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// Sayfa sayısını sadece 4'ün katları olarak belirtebiliriz.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

### Ayrıca bakınız

* class [PageSetup](../../pagesetup)
* ad alanı [Aspose.Words](../../pagesetup)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->