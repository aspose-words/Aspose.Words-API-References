---
title: FontSettings.SetFontsFolder
linktitle: SetFontsFolder
articleTitle: SetFontsFolder
second_title: .NET için Aspose.Words
description: Aspose.Words'de TrueType yazı tipi dizinini belirtmek için SetFontsFolder yönteminin nasıl kullanılacağını keşfedin, belge oluşturmayı ve yazı tipi yerleştirmeyi geliştirin.
type: docs
weight: 80
url: /tr/net/aspose.words.fonts/fontsettings/setfontsfolder/
---
## FontSettings.SetFontsFolder method

Aspose.Words'ün belgeleri işlerken veya yazı tiplerini yerleştirirken TrueType yazı tiplerini aradığı klasörü ayarlar. Bu,[`SetFontsFolders`](../setfontsfolders/) sadece bir font dizini ayarlamak için.

```csharp
public void SetFontsFolder(string fontFolder, bool recursive)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fontFolder | String | TrueType yazı tiplerini içeren klasör. |
| recursive | Boolean | Belirtilen klasörleri yazı tipleri için yinelemeli olarak taramak için doğru. |

## Örnekler

Yazı tipi kaynak dizininin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arvo";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Yazı tipi kaynaklarımız bu belgede metin için kullandığımız yazı tipini içermiyor.
// Bu dokümanı oluştururken bu yazı tipi ayarlarını kullanırsak,
// Aspose.Words, Aspose.Words'ün bulamadığı bir yazı tipine sahip metne yedek bir yazı tipi uygulayacaktır.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Varsayılan yazı tipi kaynaklarında bu belgede kullandığımız iki yazı tipi eksik.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Yeni bir font kaynağı olarak işlev görecek bir dizin ayarlamak için "SetFontsFolder" yöntemini kullanın.
// Dizin içindeki tüm yazı tipi dosyalarındaki yazı tiplerini dahil etmek için "yinelemeli" argüman olarak "false" değerini geçirin
// ilk argümanı geçiriyoruz ancak o dizinin alt klasörlerindeki hiçbir yazı tipini dahil etmiyoruz.
// Dizinimizde bulunan tüm yazı tipi dosyalarını dahil etmek için "tekrarlı" argüman olarak "true" değerini geçirin
// ilk argümanda ve alt dizinlerindeki tüm fontlarda.
FontSettings.DefaultInstance.SetFontsFolder(FontsDir, recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// "Amethysta" yazı tipi font dizininin bir alt klasöründedir.
if (recursive)
{
    Assert.AreEqual(25, newFontSources[0].GetAvailableFonts().Count);
    Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
}
else
{
    Assert.AreEqual(18, newFontSources[0].GetAvailableFonts().Count);
    Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
}

doc.Save(ArtifactsDir + "FontSettings.SetFontsFolder.pdf");

// Orijinal yazı tipi kaynaklarını geri yükleyin.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Ayrıca bakınız

* class [FontSettings](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
