---
title: MultiplePagesType Enum
linktitle: MultiplePagesType
articleTitle: MultiplePagesType
second_title: .NET için Aspose.Words
description: Verimli belge yazdırma seçenekleri için Aspose.Words.Settings.MultiplePagesType enum'unu keşfedin. Esnek yazdırma ayarlarıyla iş akışınızı optimize edin!
type: docs
weight: 6700
url: /tr/net/aspose.words.settings/multiplepagestype/
---
## MultiplePagesType enumeration

Belgenin nasıl yazdırılacağını belirtir.

```csharp
public enum MultiplePagesType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Normal | `0` | Normal yazdırma, birden fazla sayfa belirtilmemiş. |
| MirrorMargins | `1` | Karşılıklı sayfalarda sol ve sağ kenar boşluklarını değiştirir. |
| TwoPagesPerSheet | `2` | Sayfa başına iki sayfa yazdırır. |
| BookFoldPrinting | `3` | Belgenin kitap katlaması olarak yazdırılıp yazdırılmayacağını belirtir. |
| BookFoldPrintingReverse | `4` | Belgenin ters kitap katlaması olarak yazdırılıp yazdırılmayacağını belirtir. |
| Default | `0` | Varsayılan değerNormal |

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

* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)
