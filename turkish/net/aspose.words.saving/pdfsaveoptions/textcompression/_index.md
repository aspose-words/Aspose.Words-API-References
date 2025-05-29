---
title: PdfSaveOptions.TextCompression
linktitle: TextCompression
articleTitle: TextCompression
second_title: .NET için Aspose.Words
description: Belgelerinizi optimize etmek için PdfSaveOptions TextCompression özelliğini keşfedin. Verimli metin depolama ve daha hızlı yükleme için en iyi sıkıştırma türünü seçin.
type: docs
weight: 310
url: /tr/net/aspose.words.saving/pdfsaveoptions/textcompression/
---
## PdfSaveOptions.TextCompression property

Belgedeki tüm metinsel içerik için kullanılacak sıkıştırma türünü belirtir.

```csharp
public PdfTextCompression TextCompression { get; set; }
```

## Notlar

VarsayılanFlate.

Bir belgeyi sıkıştırmadan kaydederken çıktı boyutunu önemli ölçüde artırır.

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

* enum [PdfTextCompression](../../pdftextcompression/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
