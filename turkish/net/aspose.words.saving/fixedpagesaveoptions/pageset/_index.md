---
title: FixedPageSaveOptions.PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words for .NET
description: FixedPageSaveOptions PageSet mülk. Oluşturulacak sayfaları alır veya ayarlar. Varsayılan belgedeki tüm sayfalardır C#'da.
type: docs
weight: 70
url: /tr/net/aspose.words.saving/fixedpagesaveoptions/pageset/
---
## FixedPageSaveOptions.PageSet property

Oluşturulacak sayfaları alır veya ayarlar. Varsayılan, belgedeki tüm sayfalardır.

```csharp
public PageSet PageSet { get; set; }
```

## Örnekler

Tam sayfa indekslerine göre sayfaların nasıl çıkarılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgeye beş sayfa ekleyin.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// Belgenin "Save" yöntemine aktarabileceğimiz bir "XpsSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .XPS'e dönüştürme biçimini değiştirmek için.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// XPS çıktısı olarak kaydedilecek belge sayfalarının bir kümesini seçmek için "PageSet" özelliğini kullanın.
// Bu durumda, sıfır tabanlı bir dizin aracılığıyla yalnızca üç sayfayı seçeceğiz: sayfa 1, sayfa 2 ve sayfa 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

Bir belgedeki sayfaların yalnızca bazılarının PDF'ye nasıl dönüştürüleceğini gösterir.

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
    // Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
    // bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
    PdfSaveOptions options = new PdfSaveOptions();

    // Belgenin ikinci sayfadan başlayarak bir kısmını oluşturmak için "PageIndex"i "1" olarak ayarlayın.
    options.PageSet = new PageSet(1);

    // Bu belge ikinci sayfadan başlayarak yalnızca ikinci sayfayı içerecek bir sayfa içerecektir.
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

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Aşağıda, bir grup sayfayı filtrelemek için kullanabileceğimiz üç PageSet özelliği bulunmaktadır.
// belgemizi sayfa numaralarının denkliğine göre çıktı PDF belgesine kaydedeceğiz.
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
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
