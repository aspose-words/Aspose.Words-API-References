---
title: FontSettings.SetFontsSources
linktitle: SetFontsSources
articleTitle: SetFontsSources
second_title: .NET için Aspose.Words
description: Aspose.Words'deki SetFontsSources yönteminin, en iyi sonuçlar için TrueType yazı tipi kaynaklarını belirterek belge oluşturmayı nasıl geliştirdiğini keşfedin.
type: docs
weight: 100
url: /tr/net/aspose.words.fonts/fontsettings/setfontssources/
---
## SetFontsSources(*FontSourceBase[]*) {#setfontssources}

Aspose.Words'ün belgeleri işlerken veya yazı tiplerini yerleştirirken TrueType yazı tiplerini aradığı kaynakları ayarlar.

```csharp
public void SetFontsSources(FontSourceBase[] sources)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| sources | FontSourceBase[] | TrueType yazı tiplerini içeren kaynakların dizisi. |

## Notlar

Varsayılan olarak Aspose.Words sisteme yüklenen yazı tiplerini arar.

Bu özelliğin ayarlanması, daha önce yüklenen tüm yazı tiplerinin önbelleğini sıfırlar.

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

---

## SetFontsSources(*FontSourceBase[], Stream*) {#setfontssources_1}

Aspose.Words'ün TrueType yazı tiplerini aradığı kaynakları ayarlar ve ayrıca daha önce kaydedilmiş yazı tipi arama önbelleğini yükler.

```csharp
public void SetFontsSources(FontSourceBase[] sources, Stream cacheInputStream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| sources | FontSourceBase[] | TrueType yazı tiplerini içeren kaynakların dizisi. |
| cacheInputStream | Stream | Kaydedilmiş font arama önbelleğiyle giriş akışı. |

## Notlar

Önceden kaydedilmiş font arama önbelleğini yüklemek font önbelleği başlatma sürecini hızlandıracaktır. Bu özellikle font kaynaklarına erişim karmaşık olduğunda (örneğin fontlar ağ üzerinden yüklendiğinde) yararlıdır.

Font arama önbelleğini kaydederken ve yüklerken, sağlanan kaynaklardaki fontlar önbellek anahtarıyla tanımlanır. Fontlar için[`SystemFontSource`](../../systemfontsource/) Ve[`FolderFontSource`](../../folderfontsource/) önbellek anahtarı yazı tipi dosyasına giden path 'dir.[`MemoryFontSource`](../../memoryfontsource/) Ve[`StreamFontSource`](../../streamfontsource/)önbellek anahtarı, x000d_ olarak tanımlandı[`CacheKey`](../../memoryfontsource/cachekey/) Ve[`CacheKey`](../../streamfontsource/cachekey/) properties sırasıyla. Bunun için[`FileFontSource`](../../filefontsource/) önbellek anahtarı ya[`CacheKey`](../../filefontsource/cachekey/) özelliği veya bir dosya yolu[`CacheKey`](../../filefontsource/cachekey/) dır`hükümsüz`.

Önbelleği yüklerken, önbelleğin kaydedildiği zamandakiyle aynı yazı tipi kaynaklarını sağlamanız şiddetle önerilir. Yazı tipi kaynaklarında yapılan herhangi bir değişiklik (örneğin, yeni yazı tipleri eklemek, yazı tipi dosyalarını taşımak veya önbellek anahtarını değiştirmek) Aspose.Words tarafından yanlış yazı tipi çözümlemesine yol açabilir.

## Örnekler

Yazı tipi önbelleği başlatma işleminin nasıl hızlandırılacağını gösterir.

```csharp
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
/// Font verilerini hafızada saklamak yerine yalnızca gerektiğinde yükleyin
/// "FontSettings" nesnesinin tüm yaşam süresi boyunca.
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
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
