---
title: FontSettings.SetFontsFolder
second_title: Aspose.Words for .NET API Referansı
description: FontSettings yöntem. Aspose.Wordsün belgeleri oluştururken veya yazı tiplerini gömerken TrueType yazı tiplerini aradığı klasörü ayarlar. BuSetFontsFolders yalnızca bir yazı tipi dizini ayarlamak için.
type: docs
weight: 80
url: /tr/net/aspose.words.fonts/fontsettings/setfontsfolder/
---
## FontSettings.SetFontsFolder method

Aspose.Words'ün belgeleri oluştururken veya yazı tiplerini gömerken TrueType yazı tiplerini aradığı klasörü ayarlar. Bu,[`SetFontsFolders`](../setfontsfolders/) yalnızca bir yazı tipi dizini ayarlamak için.

```csharp
public void SetFontsFolder(string fontFolder, bool recursive)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fontFolder | String | TrueType yazı tiplerini içeren klasör. |
| recursive | Boolean | Yazı tipleri için belirtilen klasörleri yinelemeli olarak taramak için True. |

### Örnekler

Bir yazı tipi kaynak dizininin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arvo";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Yazı tipi kaynaklarımız bu belgede metin için kullandığımız yazı tipini içermiyor.
// Bu belgeyi render ederken bu font ayarlarını kullanırsak,
// Aspose.Words, Aspose.Words'ün bulamadığı bir yazı tipine sahip metne bir yedek yazı tipi uygulayacaktır.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Varsayılan yazı tipi kaynaklarında bu belgede kullandığımız iki yazı tipi eksik.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Yeni yazı tipi kaynağı görevi görecek bir dizin ayarlamak için "SetFontsFolder" yöntemini kullanın.
// Dizindeki tüm yazı tipi dosyalarından yazı tiplerini dahil etmek için "özyinelemeli" argüman olarak "yanlış"ı iletin
// ilk argümanı aktarıyoruz ancak o dizinin alt klasörlerinin hiçbirine yazı tipi eklemiyoruz.
// İlettiğimiz dizindeki tüm yazı tipi dosyalarını dahil etmek için "özyinelemeli" argüman olarak "doğru"yu iletin
// ilk argümanda ve alt dizinlerindeki tüm yazı tiplerinde.
FontSettings.DefaultInstance.SetFontsFolder(FontsDir, recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// "Amethysta" yazı tipi, yazı tipi dizininin bir alt klasöründe bulunur.
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
* ad alanı [Aspose.Words.Fonts](../../fontsettings/)
* toplantı [Aspose.Words](../../../)


