---
title: PageSet.Odd
linktitle: Odd
articleTitle: Odd
second_title: .NET için Aspose.Words
description: Verimli belge yönetimi için belgenizdeki tüm tek sayfalara orijinal sıralarında kolayca ulaşmak amacıyla PageSet Odd özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/pageset/odd/
---
## PageSet.Odd property

Belgenin tüm tek sayfalarını orijinal sıralarında içeren bir küme alır.

```csharp
public static PageSet Odd { get; }
```

## Notlar

Sayfa dizinleri sıfır tabanlı olduğundan tek sayfaların dizinleri çifttir.

## Örnekler

Belgeden Tek sayfaların nasıl dışa aktarılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 5; i++)
{
    builder.Writeln($"Page {i + 1} ({(i % 2 == 0 ? "odd" : "even")})");
    if (i < 4)
        builder.InsertBreak(BreakType.PageBreak);
}

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Aşağıda, bir sayfa kümesini filtrelemek için kullanabileceğimiz üç PageSet özelliği bulunmaktadır
// sayfa numaralarının eşitliğine göre çıktı PDF belgesinde kaydetmek üzere belgemiz.
// 1 - Yalnızca çift sayılı sayfaları kaydet:
options.PageSet = PageSet.Even;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.Even.pdf", options);

// 2 - Yalnızca tek numaralı sayfaları kaydet:
options.PageSet = PageSet.Odd;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.Odd.pdf", options);

// 3 - Her sayfayı kaydet:
options.PageSet = PageSet.All;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.All.pdf", options);
```

### Ayrıca bakınız

* class [PageSet](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
