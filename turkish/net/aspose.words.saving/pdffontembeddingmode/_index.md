---
title: PdfFontEmbeddingMode Enum
linktitle: PdfFontEmbeddingMode
articleTitle: PdfFontEmbeddingMode
second_title: .NET için Aspose.Words
description: PDF'lerde en iyi font yerleştirme için Aspose.Words.PdfFontEmbeddingMode enum'unu keşfedin. Belge kalitesini artırın ve tutarlı metin görüntülemesini sağlayın.
type: docs
weight: 6260
url: /tr/net/aspose.words.saving/pdffontembeddingmode/
---
## PdfFontEmbeddingMode enumeration

Aspose.Words'ün fontları nasıl gömeceğini belirtir.

```csharp
public enum PdfFontEmbeddingMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| EmbedAll | `0` | Aspose.Words tüm yazı tiplerini gömer. |
| EmbedNonstandard | `1` | Aspose.Words, standart Windows yazı tipleri Arial ve Times New Roman hariç tüm yazı tiplerini gömer. Bu modda yalnızca Arial ve Times New Roman yazı tipleri etkilenir çünkü MS Word, belgeyi PDF'ye kaydederken yalnızca bu yazı tiplerini gömemez. |
| EmbedNone | `2` | Aspose.Words hiçbir yazı tipini gömmüyor. |

## Örnekler

Aspose.Words'ün Arial ve Times New Roman yazı tiplerini bir PDF belgesine yerleştirmeyi nasıl atlayacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "Arial" standart bir yazı tipidir ve "Courier New" standart dışı bir yazı tipidir.
builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();
// Çıktı PDF'ine her gömülü yazı tipinin her glifini gömmek için "EmbedFullFonts" özelliğini "true" olarak ayarlayın.
options.EmbedFullFonts = true;
// Çıktı PDF'ine tüm yazı tiplerini yerleştirmek için "FontEmbeddingMode" özelliğini "EmbedAll" olarak ayarlayın.
// Çıktı PDF'ine yalnızca standart olmayan yazı tiplerinin gömülmesine izin vermek için "FontEmbeddingMode" özelliğini "EmbedNonstandard" olarak ayarlayın.
// Çıktı PDF'ine hiçbir yazı tipini gömmemek için "FontEmbeddingMode" özelliğini "EmbedNone" olarak ayarlayın.
options.FontEmbeddingMode = pdfFontEmbeddingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf", options);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
