---
title: StreamFontSource.CacheKey
linktitle: CacheKey
articleTitle: CacheKey
second_title: .NET için Aspose.Words
description: StreamFontSource CacheKey özelliğini keşfedin, daha hızlı yükleme süreleri ve gelişmiş performans için verimli önbelleğe alma ile font yönetiminizi optimize edin.
type: docs
weight: 10
url: /tr/net/aspose.words.fonts/streamfontsource/cachekey/
---
## StreamFontSource.CacheKey property

Önbellekteki bu kaynağın anahtarı.

```csharp
public string CacheKey { get; }
```

## Notlar

Bu anahtar, font arama önbelleğini kaydederken/yüklerken önbellek öğesini tanımlamak için kullanılır. [`SaveSearchCache`](../../fontsettings/savesearchcache/) Ve[`SetFontsSources`](../../fontsettings/setfontssources/) yöntemler.

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

* class [StreamFontSource](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
