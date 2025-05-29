---
title: PdfSaveOptions.FontEmbeddingMode
linktitle: FontEmbeddingMode
articleTitle: FontEmbeddingMode
second_title: .NET için Aspose.Words
description: PDF'nizin font yerleştirmesini optimize etmek için PdfSaveOptions FontEmbeddingMode özelliğini keşfedin. Belge kalitesini ve uyumluluğu zahmetsizce artırın!
type: docs
weight: 170
url: /tr/net/aspose.words.saving/pdfsaveoptions/fontembeddingmode/
---
## PdfSaveOptions.FontEmbeddingMode property

Yazı tipi yerleştirme modunu belirtir.

```csharp
public PdfFontEmbeddingMode FontEmbeddingMode { get; set; }
```

## Notlar

Varsayılan değer:EmbedAll.

Bu ayar yalnızca ANSI (Windows-1252) kodlamasındaki metin için çalışır. Belge ANSI olmayan metin içeriyorsa, karşılık gelen yazı tipleri bu ayardan bağımsız olarak gömülür.

PDF/A ve PDF/UA uyumluluğu tüm yazı tiplerinin gömülmesini gerektirir. EmbedAll to PDF/A ve PDF/UA kaydedilirken bu değer otomatik olarak kullanılacaktır.

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

* enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
