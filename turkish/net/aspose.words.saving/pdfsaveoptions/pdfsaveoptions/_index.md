---
title: PdfSaveOptions
linktitle: PdfSaveOptions
articleTitle: PdfSaveOptions
second_title: .NET için Aspose.Words
description: Belgelerinizi yüksek kaliteli PDF formatında zahmetsizce başlatmak ve kaydetmek için tasarlanmış PdfSaveOptions oluşturucusunu keşfedin. İş akışınızı bugün kolaylaştırın!
type: docs
weight: 10
url: /tr/net/aspose.words.saving/pdfsaveoptions/pdfsaveoptions/
---
## PdfSaveOptions constructor

Bu sınıfın, içindeki bir belgeyi kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Pdf biçim.

```csharp
public PdfSaveOptions()
```

## Örnekler

Bir belgeyi PDF'e dönüştürürken yazı tiplerini gömerken alt kümelemenin nasıl etkinleştirileceğini veya devre dışı bırakılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Bu belgedeki her iki yazı tipine de erişebildiğimizden emin olmak için yazı tipi kaynaklarımızı yapılandırın.
FontSourceBase[] originalFontsSources = FontSettings.DefaultInstance.GetFontsSources();
Aspose.Words.Fonts.FolderFontSource folderFontSource =
    new Aspose.Words.Fonts.FolderFontSource(FontsDir, true);
FontSettings.DefaultInstance.SetFontsSources(new[] { originalFontsSources[0], folderFontSource });

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(fontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Belgemiz özel bir yazı tipi içerdiğinden, çıktı belgesine gömülmesi istenebilir.
// Çıktı PDF'ine her gömülü yazı tipinin her glifini gömmek için "EmbedFullFonts" özelliğini "true" olarak ayarlayın.
// Belgenin boyutu çok büyük olabilir, ancak PDF'i düzenlediğimizde tüm yazı tiplerini tam olarak kullanabiliriz.
// Alt kümelemeyi yazı tiplerine uygulamak ve yalnızca glifleri kaydetmek için "EmbedFullFonts" özelliğini "false" olarak ayarlayın
// belgenin kullandığı. Dosya önemli ölçüde daha küçük olacak,
// ancak belgeyi düzenlersek herhangi bir özel yazı tipine erişmemiz gerekebilir.
options.EmbedFullFonts = embedFullFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf", options);

// Orijinal yazı tipi kaynaklarını geri yükleyin.
FontSettings.DefaultInstance.SetFontsSources(originalFontsSources);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
