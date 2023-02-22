---
title: FontSettings.SetFontsSources
second_title: Aspose.Words for .NET API Referansı
description: FontSettings yöntem. Aspose.Wordsün belgeleri oluştururken veya yazı tiplerini gömerken TrueType yazı tiplerini aradığı kaynakları ayarlar.
type: docs
weight: 100
url: /tr/net/aspose.words.fonts/fontsettings/setfontssources/
---
## SetFontsSources(FontSourceBase[]) {#setfontssources}

Aspose.Words'ün belgeleri oluştururken veya yazı tiplerini gömerken TrueType yazı tiplerini aradığı kaynakları ayarlar.

```csharp
public void SetFontsSources(FontSourceBase[] sources)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| sources | FontSourceBase[] | TrueType yazı tiplerini içeren bir dizi kaynak. |

### Notlar

Aspose.Words varsayılan olarak sistemde kurulu olan yazı tiplerini arar.

Bu özelliğin ayarlanması, önceden yüklenmiş tüm yazı tiplerinin önbelleğini sıfırlar.

### Örnekler

Mevcut yazı tipi kaynaklarımıza nasıl yazı tipi kaynağı ekleneceğini gösterir.

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

// Varsayılan yazı tipi kaynağında, belgemizde kullandığımız yazı tiplerinden ikisi eksik.
// Bu belgeyi kaydettiğimizde, Aspose.Words, erişilemeyen yazı tipleriyle formatlanmış tüm metinlere yedek yazı tipleri uygulayacaktır.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Fontları içeren bir klasörden bir font kaynağı oluşturun.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Özel yazı tiplerimizin yanı sıra orijinal yazı tipi kaynaklarını içeren yeni bir yazı tipi kaynakları dizisi uygulayın.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// Belgeyi PDF'ye dönüştürmeden önce Aspose.Words'ün gerekli tüm yazı tiplerine erişimi olduğunu doğrulayın.
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
* ad alanı [Aspose.Words.Fonts](../../fontsettings/)
* toplantı [Aspose.Words](../../../)

---

## SetFontsSources(FontSourceBase[], Stream) {#setfontssources_1}

Aspose.Words'ün TrueType yazı tiplerini aradığı kaynakları ayarlar ve ek olarak önceden kaydedilmiş yazı tipi arama önbelleğini yükler.

```csharp
public void SetFontsSources(FontSourceBase[] sources, Stream cacheInputStream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| sources | FontSourceBase[] | TrueType yazı tiplerini içeren bir dizi kaynak. |
| cacheInputStream | Stream | Kaydedilmiş yazı tipi arama önbelleği ile giriş akışı. |

### Notlar

Önceden kaydedilmiş yazı tipi arama önbelleğini yüklemek, yazı tipi önbelleği başlatma sürecini hızlandıracaktır. Özellikle yazı tipi kaynaklarına erişim karmaşık olduğunda (örneğin yazı tipleri ağ üzerinden yüklendiğinde) yararlıdır.

Yazı tipi arama önbelleği kaydedilirken ve yüklenirken, sağlanan kaynaklardaki yazı tipleri önbellek anahtarı aracılığıyla tanımlanır. [`SystemFontSource`](../../systemfontsource/) ve[`FolderFontSource`](../../folderfontsource/) önbellek anahtarı, yazı tipi dosyasının path yoludur. İçin[`MemoryFontSource`](../../memoryfontsource/) ve[`StreamFontSource`](../../streamfontsource/) önbellek anahtarı, tanımlı [`CacheKey`](../../memoryfontsource/cachekey/) ve[`CacheKey`](../../streamfontsource/cachekey/) Properties sırasıyla. İçin[`FileFontSource`](../../filefontsource/) önbellek anahtarı ya[`CacheKey`](../../filefontsource/cachekey/) özelliği veya bir dosya yolu[`CacheKey`](../../filefontsource/cachekey/) dır-dir **hükümsüz**.

Önbelleği yüklerken, önbelleğin kaydedildiği andaki yazı tipi kaynaklarının aynısını sağlamanız önemle tavsiye edilir. Yazı tipi kaynaklarındaki herhangi bir değişiklik (örneğin, yeni yazı tipleri ekleme, yazı tipi dosyalarını taşıma veya önbellek anahtarını değiştirme) hatalı yazı tipine neden olabilir. Aspose.Words tarafından çözümleniyor.

### Örnekler

Yazı tipi önbelleği başlatma işleminin nasıl hızlandırılacağını gösterir.

```csharp
[Test]
public void LoadFontSearchCache()
{
    const string cacheKey1 = "Arvo";
    const string cacheKey2 = "Arvo-Bold";
    FontSettings parsedFonts = new FontSettings();
    FontSettings loadedCache = new FontSettings();

    parsedFonts.SetFontsSources(new FontSourceBase[]
    {
        new FileFontSource(FontsDir + "Arvo-Regular.ttf", 0, cacheKey1),
        new FileFontSource(FontsDir + "Arvo-Bold.ttf", 0, cacheKey2)
    });

    using (MemoryStream cacheStream = new MemoryStream())
    {
        parsedFonts.SaveSearchCache(cacheStream);
        loadedCache.SetFontsSources(new FontSourceBase[]
        {
            new SearchCacheStream(cacheKey1),                    
            new MemoryFontSource(File.ReadAllBytes(FontsDir + "Arvo-Bold.ttf"), 0, cacheKey2)
        }, cacheStream);
    }

    Assert.AreEqual(parsedFonts.GetFontsSources().Length, loadedCache.GetFontsSources().Length);
}

/// <summary>
/// Yazı tipi verilerini bellekte saklamak yerine yalnızca gerektiğinde yükleyin
/// "FontSettings" nesnesinin tüm kullanım ömrü boyunca.
/// </summary>
private class SearchCacheStream : StreamFontSource
{
    public SearchCacheStream(string cacheKey):base(0, cacheKey)
    {
    }

    public override Stream OpenFontDataStream()
    {
        return File.OpenRead(FontsDir + "Arvo-Regular.ttf");
    }
}
```

### Ayrıca bakınız

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* ad alanı [Aspose.Words.Fonts](../../fontsettings/)
* toplantı [Aspose.Words](../../../)


