---
title: PdfTextCompression Enum
linktitle: PdfTextCompression
articleTitle: PdfTextCompression
second_title: .NET için Aspose.Words
description: Verimli PDF içerik sıkıştırması, kaliteyi korurken dosya boyutunu ve performansını artırmak için Aspose.Words.PdfTextCompression enum'unu keşfedin.
type: docs
weight: 6330
url: /tr/net/aspose.words.saving/pdftextcompression/
---
## PdfTextCompression enumeration

PDF dosyasındaki resimler hariç tüm içeriklere uygulanan sıkıştırma türünü belirtir.

```csharp
public enum PdfTextCompression
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Sıkıştırma yok. |
| Flate | `1` | Düz (ZIP) sıkıştırma. |

## Örnekler

Bir belgeyi PDF'e kaydederken metin sıkıştırmanın nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Herhangi bir uygulama yapmamak için "TextCompression" özelliğini "PdfTextCompression.None" olarak ayarlayın
// Belgeyi PDF'e kaydettiğimizde metne sıkıştırma.
// ZIP sıkıştırmasını uygulamak için "TextCompression" özelliğini "PdfTextCompression.Flate" olarak ayarlayın
// Belgeyi PDF'e kaydettiğimizde metne. Belge ne kadar büyükse, bunun etkisi de o kadar büyük olacaktır.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
