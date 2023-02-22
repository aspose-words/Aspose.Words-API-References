---
title: FixedPageSaveOptions.PageSet
second_title: Aspose.Words for .NET API Referansı
description: FixedPageSaveOptions mülk. Oluşturulacak sayfaları alır veya ayarlar. Varsayılan belgedeki tüm sayfalardır.
type: docs
weight: 70
url: /tr/net/aspose.words.saving/fixedpagesaveoptions/pageset/
---
## FixedPageSaveOptions.PageSet property

Oluşturulacak sayfaları alır veya ayarlar. Varsayılan, belgedeki tüm sayfalardır.

```csharp
public PageSet PageSet { get; set; }
```

### Örnekler

Tam sayfa dizinlerine göre sayfaların nasıl çıkarılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgeye beş sayfa ekleyin.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "XpsSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .XPS'ye dönüştürme şeklini değiştirmek için.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// XPS çıktısına kaydedilecek belge sayfaları kümesini seçmek için "PageSet" özelliğini kullanın.
// Bu durumda, sıfır tabanlı bir dizin aracılığıyla yalnızca üç sayfa seçeceğiz: sayfa 1, sayfa 2 ve sayfa 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

Bir belgedeki yalnızca bazı sayfaların nasıl PDF'ye dönüştürüleceğini gösterir.

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
    // Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
    // bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
    PdfSaveOptions options = new PdfSaveOptions();

    // İkinci sayfadan başlayarak belgenin bir bölümünü oluşturmak için "PageIndex"i "1" olarak ayarlayın.
    options.PageSet = new PageSet(1);

    // Bu belge, ikinci sayfadan başlayarak yalnızca ikinci sayfayı içerecek olan bir sayfa içerecektir.
    doc.Save(stream, options);
}
```

Tek sayfaların belgeden nasıl dışa aktarılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 5; i++)
{
    builder.Writeln($"Page {i + 1} ({(i % 2 == 0 ? "odd" : "even")})");
    if (i < 4)
        builder.InsertBreak(BreakType.PageBreak);
}

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Aşağıda, bir sayfa kümesini filtrelemek için kullanabileceğimiz üç PageSet özelliği bulunmaktadır.
// sayfa numaralarının paritesine göre bir çıktı PDF belgesine kaydedilecek belgemiz.
// 1 - Yalnızca çift sayılı sayfaları kaydedin:
options.PageSet = PageSet.Even;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.Even.pdf", options);

// 2 - Yalnızca tek sayılı sayfaları kaydedin:
options.PageSet = PageSet.Odd;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.Odd.pdf", options);

// 3 - Her sayfayı kaydet:
options.PageSet = PageSet.All;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.All.pdf", options);
```

### Ayrıca bakınız

* class [PageSet](../../pageset/)
* class [FixedPageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../fixedpagesaveoptions/)
* toplantı [Aspose.Words](../../../)


