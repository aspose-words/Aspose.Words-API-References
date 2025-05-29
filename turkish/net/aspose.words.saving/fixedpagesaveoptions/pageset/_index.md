---
title: FixedPageSaveOptions.PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: .NET için Aspose.Words
description: FixedPageSaveOptions PageSet ile belgenizin işlenmesini kontrol edin. Belirli sayfaları kolayca seçin veya sorunsuz çıktı için hepsini seçin. İş akışınızı optimize edin!
type: docs
weight: 70
url: /tr/net/aspose.words.saving/fixedpagesaveoptions/pageset/
---
## FixedPageSaveOptions.PageSet property

İşlenecek sayfaları alır veya ayarlar. Varsayılan, belgedeki tüm sayfalardır.

```csharp
public PageSet PageSet { get; set; }
```

## Örnekler

Sayfaların kesin sayfa indekslerine göre nasıl çıkarılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgeye beş sayfa ekle.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "XpsSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .XPS'e nasıl dönüştüreceğini değiştirmek için.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// Çıkış XPS'e kaydedilecek belgenin sayfalarının bir kümesini seçmek için "PageSet" özelliğini kullanın.
// Bu durumda, sıfır tabanlı bir dizin aracılığıyla yalnızca üç sayfa seçeceğiz: sayfa 1, sayfa 2 ve sayfa 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

Bir belgedeki sayfaların yalnızca bir kısmının PDF'e nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

using (Stream stream = File.Create(ArtifactsDir + "PdfSaveOptions.OnePage.pdf"))
{
    // Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
    // bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
    PdfSaveOptions options = new PdfSaveOptions();

    // Belgenin ikinci sayfadan başlayarak bir kısmını işlemek için "PageIndex" değerini "1" olarak ayarlayın.
    options.PageSet = new PageSet(1);

    // Bu belge, ikinci sayfadan başlayarak tek bir sayfadan oluşacak ve ikinci sayfada yalnızca ikinci sayfa yer alacaktır.
    doc.Save(stream, options);
}
```

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

* class [PageSet](../../pageset/)
* class [FixedPageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
