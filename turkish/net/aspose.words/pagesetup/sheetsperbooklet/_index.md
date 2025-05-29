---
title: PageSetup.SheetsPerBooklet
linktitle: SheetsPerBooklet
articleTitle: SheetsPerBooklet
second_title: .NET için Aspose.Words
description: Kitapçık sayfa sayılarını kolayca yönetmek, belge düzeninizi ve yazdırma verimliliğinizi artırmak için PageSetup SheetsPerBooklet özelliğini keşfedin.
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

// 16 sayfaya yayılacak metni ekleyin.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Belgeyi kitap katlaması biçiminde yazdırmak için ilk bölümün "PageSetup" özelliğini yapılandırın.
// Bu belgeyi her iki tarafa da yazdırdığımızda sayfaları istiflemek için kullanabiliriz
// ve hepsini aynı anda ortadan katlayın. Belgenin içerikleri bir kitap katlaması şeklinde sıralanacaktır.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// Sayfa sayısını yalnızca 4'ün katları şeklinde belirtebiliriz.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

### Ayrıca bakınız

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
