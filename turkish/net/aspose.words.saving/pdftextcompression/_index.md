---
title: Enum PdfTextCompression
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.PdfTextCompression Sıralama. PDF dosyasındaki resimler hariç tüm içeriğe uygulanan sıkıştırma türünü belirtir.
type: docs
weight: 5530
url: /tr/net/aspose.words.saving/pdftextcompression/
---
## PdfTextCompression enumeration

PDF dosyasındaki resimler hariç tüm içeriğe uygulanan sıkıştırma türünü belirtir.

```csharp
public enum PdfTextCompression
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Sıkıştırma yok. |
| Flate | `1` | Düzleştir (ZIP) sıkıştırma. |

### Örnekler

Bir belgeyi PDF'ye kaydederken metin sıkıştırmanın nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Herhangi bir uygulama yapmamak için "TextCompression" özelliğini "PdfTextCompression.None" olarak ayarlayın
// belgeyi PDF'ye kaydettiğimizde metne sıkıştırma.
// ZIP sıkıştırmasını uygulamak için "TextCompression" özelliğini "PdfTextCompression.Flate" olarak ayarlayın
// belgeyi PDF'ye kaydettiğimizde metne. Belge ne kadar büyük olursa, bunun etkisi de o kadar büyük olur.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


