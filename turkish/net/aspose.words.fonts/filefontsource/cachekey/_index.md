---
title: FileFontSource.CacheKey
linktitle: CacheKey
articleTitle: CacheKey
second_title: .NET için Aspose.Words
description: Verimli font yönetimi ve gelişmiş performans için optimize edilmiş önbelleğe almanın anahtarı olan FileFontSource CacheKey özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.fonts/filefontsource/cachekey/
---
## FileFontSource.CacheKey property

Önbellekteki bu kaynağın anahtarı.

```csharp
public string CacheKey { get; }
```

## Notlar

Bu anahtar, font arama önbelleğini kaydederken/yüklerken önbellek öğesini tanımlamak için kullanılır.[`SaveSearchCache`](../../fontsettings/savesearchcache/) ve [`SetFontsSources`](../../fontsettings/setfontssources/) Yöntemler.

Anahtar belirtilmemişse o zaman[`FilePath`](../filepath/) anahtar olarak kullanılacaktır.

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

* class [FileFontSource](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
