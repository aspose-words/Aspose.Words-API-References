---
title: FontSettings.GetFontsSources
linktitle: GetFontsSources
articleTitle: GetFontsSources
second_title: .NET için Aspose.Words
description: Aspose.Words'deki TrueType fontları için kaynak dizisine kolayca erişmek için FontSettings GetFontsSources yöntemini keşfedin. Font yönetiminizi bugün optimize edin!
type: docs
weight: 50
url: /tr/net/aspose.words.fonts/fontsettings/getfontssources/
---
## FontSettings.GetFontsSources method

Aspose.Words'ün TrueType yazı tiplerini aradığı kaynakların listesini içeren dizinin bir kopyasını alır.

```csharp
public FontSourceBase[] GetFontsSources()
```

### Geri dönüş değeri

Güncel yazı tipi kaynaklarının bir kopyası.

## Notlar

Döndürülen değer, Aspose.Words'ün kullandığı verilerin bir kopyasıdır. Döndürülen dizideki entrys öğesini değiştirirseniz, belgenin işlenmesi üzerinde hiçbir etkisi olmaz. Yeni fontu belirtmek için resources öğesini kullanın[`SetFontsSources`](../setfontssources/) yöntem.

## Örnekler

Mevcut font kaynaklarımıza nasıl font kaynağı ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);

Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Varsayılan yazı tipi kaynağında, belgemizde kullandığımız iki yazı tipi eksik.
// Bu belgeyi kaydettiğimizde, Aspose.Words erişilemeyen yazı tipleriyle biçimlendirilmiş tüm metinlere yedek yazı tiplerini uygulayacaktır.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Fontları içeren bir klasörden bir font kaynağı oluştur.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Orijinal yazı tipi kaynaklarının yanı sıra özel yazı tiplerimizi de içeren yeni bir yazı tipi kaynakları dizisi uygulayın.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// Belgeyi PDF'e dönüştürmeden önce Aspose.Words'ün tüm gerekli yazı tiplerine erişiminin olduğunu doğrulayın.
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.True(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

// Orijinal yazı tipi kaynaklarını geri yükleyin.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Ayrıca bakınız

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
