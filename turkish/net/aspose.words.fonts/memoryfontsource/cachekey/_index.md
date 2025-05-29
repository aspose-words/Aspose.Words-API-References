---
title: MemoryFontSource.CacheKey
linktitle: CacheKey
articleTitle: CacheKey
second_title: .NET için Aspose.Words
description: MemoryFontSource CacheKey özelliğini keşfedin; gelişmiş performans ve optimize edilmiş bellek yönetimi için benzersiz bir anahtarla verimli önbelleğe almanın kilidini açın.
type: docs
weight: 20
url: /tr/net/aspose.words.fonts/memoryfontsource/cachekey/
---
## MemoryFontSource.CacheKey property

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

* class [MemoryFontSource](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
