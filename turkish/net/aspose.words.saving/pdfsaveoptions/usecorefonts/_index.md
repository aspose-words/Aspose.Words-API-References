---
title: PdfSaveOptions.UseCoreFonts
linktitle: UseCoreFonts
articleTitle: UseCoreFonts
second_title: Aspose.Words for .NET
description: PdfSaveOptions UseCoreFonts mülk. TrueType yazı tiplerinin Arial Times New Roman Courier New ve Sembol ile temel PDF Type 1 yazı tipleriyle değiştirilip değiştirilmeyeceğini belirleyen bir değer alır veya ayarlar C#'da.
type: docs
weight: 310
url: /tr/net/aspose.words.saving/pdfsaveoptions/usecorefonts/
---
## PdfSaveOptions.UseCoreFonts property

TrueType yazı tiplerinin Arial, Times New Roman, Courier New ve Sembol ile temel PDF Type 1 yazı tipleriyle değiştirilip değiştirilmeyeceğini belirleyen bir değer alır veya ayarlar.

```csharp
public bool UseCoreFonts { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ` . Bu değer şu şekilde ayarlandığında`doğru` Arial, Times New Roman, Courier New ve Sembol yazı tipleri, PDF belgesinde karşılık gelen temel Type 1 yazı tipiyle değiştirildi.

Çekirdek PDF yazı tiplerinin veya bunların yazı tipi ölçümlerinin ve uygun ikame yazı tiplerinin herhangi bir PDF görüntüleyici uygulamasında mevcut olması gerekir.

Bu ayar yalnızca ANSI (Windows-1252) kodlamasındaki metin için çalışır. ANSI olmayan metin, bu ayardan bağımsız olarak gömülü TrueType yazı tipiyle yazılacak olacaktır.

PDF/A ve PDF/UA uyumluluğu tüm yazı tiplerinin gömülü olmasını gerektirir.`YANLIŞ` PDF/A ve PDF/UA'ya kaydederken değer otomatik olarak kullanılacak .

PDF 2.0 formatında kaydederken çekirdek yazı tipleri desteklenmez.`YANLIŞ` PDF 2.0'a kaydederken değer otomatik olarak kullanılacak olacaktır.

Bu seçeneğin önceliği daha yüksektir[`FontEmbeddingMode`](../fontembeddingmode/) seçenek.

## Örnekler

PDF Type 1 yazı tipi değişiminin nasıl etkinleştirildiğini/devre dışı bırakıldığını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Bazı yazı tiplerini değiştirmek için "UseCoreFonts" özelliğini "true" olarak ayarlayın,
// belgemizdeki iki yazı tipini PDF Type 1 eşdeğerleriyle birlikte dahil ediyoruz.
// PDF Type 1 yazı tiplerini uygulamamak için "UseCoreFonts" özelliğini "false" olarak ayarlayın.
options.UseCoreFonts = useCoreFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedCoreFonts.pdf", options);

if (useCoreFonts)
    Assert.That(3000, Is.AtLeast(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedCoreFonts.pdf").Length));
else
    Assert.That(30000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedCoreFonts.pdf").Length));
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
