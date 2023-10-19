---
title: PageSetup.SheetsPerBooklet
linktitle: SheetsPerBooklet
articleTitle: SheetsPerBooklet
second_title: Aspose.Words for .NET
description: PageSetup SheetsPerBooklet mülk. Her kitapçığa dahil edilecek sayfa sayısını döndürür veya ayarlar C#'da.
type: docs
weight: 400
url: /tr/net/aspose.words/pagesetup/sheetsperbooklet/
---
## PageSetup.SheetsPerBooklet property

Her kitapçığa dahil edilecek sayfa sayısını döndürür veya ayarlar.

```csharp
public int SheetsPerBooklet { get; set; }
```

## Örnekler

Kitap katlaması olarak yazdırılabilecek bir belgenin nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();

// 16 sayfaya yayılan metni ekleyin.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Belgeyi kitap katlama biçiminde yazdırmak için ilk bölümün "PageSetup" özelliğini yapılandırın.
// Bu belgeyi her iki tarafa da yazdırdığımızda sayfaları istiflemek için alabiliriz
// ve hepsini aynı anda ortadan katlayın. Belgenin içeriği bir kitap katlama şeklinde sıralanacaktır.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// Sayfa sayısını yalnızca 4'ün katları olarak belirtebiliriz.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

### Ayrıca bakınız

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
