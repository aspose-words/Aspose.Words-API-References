---
title: PdfSaveOptions.EmbedFullFonts
linktitle: EmbedFullFonts
articleTitle: EmbedFullFonts
second_title: Aspose.Words for .NET
description: PdfSaveOptions EmbedFullFonts mülk. Fontların elde edilen PDF belgelerine nasıl gömüleceğini kontrol eder C#'da.
type: docs
weight: 120
url: /tr/net/aspose.words.saving/pdfsaveoptions/embedfullfonts/
---
## PdfSaveOptions.EmbedFullFonts property

Fontların elde edilen PDF belgelerine nasıl gömüleceğini kontrol eder.

```csharp
public bool EmbedFullFonts { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ`bu, yazı tiplerinin yerleştirmeden önce alt kümelere ayrıldığı anlamına gelir. Çıktı dosyasının boyutunu daha küçük tutmak istiyorsanız alt kümeleme kullanışlıdır. Alt kümeleme, all kullanılmayan glifleri bir yazı tipinden kaldırır.

Bu değer şu şekilde ayarlandığında`doğru`, tam bir yazı tipi dosyası, alt kümesi olmadan PDF'ye gömülür. Bu, çıktı dosyalarının daha büyük olmasına neden olur, ancak ortaya çıkan PDF'yi daha sonra düzenlemek (örneğin daha fazla metin eklemek) istediğinizde yararlı bir seçenek olabilir.

Bazı yazı tipleri büyüktür (birkaç megabayt) ve bunları subsetting olmadan gömmek, büyük çıktı belgeleriyle sonuçlanacaktır.

## Örnekler

Bir belgeyi PDF'ye dönüştürürken yazı tiplerini gömerken alt kümelemenin nasıl etkinleştirileceğini veya devre dışı bırakılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Bu belgedeki her iki yazı tipine de erişebildiğimizden emin olmak için yazı tipi kaynaklarımızı yapılandırın.
FontSourceBase[] originalFontsSources = FontSettings.DefaultInstance.GetFontsSources();
Aspose.Words.Fonts.FolderFontSource folderFontSource = new Aspose.Words.Fonts.FolderFontSource(FontsDir, true);
FontSettings.DefaultInstance.SetFontsSources(new[] { originalFontsSources[0], folderFontSource });

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(fontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Belgemiz özel bir yazı tipi içerdiğinden, çıktı belgesine gömmek istenebilir.
// Çıktı PDF'sine her gömülü yazı tipinin her glifini gömmek için "EmbedFullFonts" özelliğini "true" olarak ayarlayın.
// Belgenin boyutu çok büyüyebilir ancak PDF'yi düzenlersek tüm yazı tiplerini tam olarak kullanabiliriz.
// Fontlara alt kümeleme uygulamak ve yalnızca glifleri kaydetmek için "EmbedFullFonts" özelliğini "false" olarak ayarlayın
// belgenin kullandığı. Dosya oldukça küçük olacak,
// ancak belgeyi düzenlersek herhangi bir özel yazı tipine erişmemiz gerekebilir.
options.EmbedFullFonts = embedFullFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf", options);

if (embedFullFonts)
    Assert.That(500000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf").Length));
else
    Assert.That(25000, Is.AtLeast(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf").Length));

// Orijinal yazı tipi kaynaklarını geri yükleyin.
FontSettings.DefaultInstance.SetFontsSources(originalFontsSources);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
