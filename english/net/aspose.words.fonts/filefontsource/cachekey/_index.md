---
title: FileFontSource.CacheKey
linktitle: CacheKey
articleTitle: CacheKey
second_title: Aspose.Words for .NET
description: FileFontSource CacheKey property. The key of this source in the cache in C#.
type: docs
weight: 20
url: /net/aspose.words.fonts/filefontsource/cachekey/
---
## FileFontSource.CacheKey property

The key of this source in the cache.

```csharp
public string CacheKey { get; }
```

## Remarks

This key is used to identify cache item when saving/loading font search cache with [`SaveSearchCache`](../../fontsettings/savesearchcache/) and [`SetFontsSources`](../../fontsettings/setfontssources/) methods.

If key is not specified then [`FilePath`](../filepath/) will be used as a key instead.

## Examples

Shows how to speed up the font cache initialization process.

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
/// Load the font data only when required instead of storing it in the memory
/// for the entire lifetime of the "FontSettings" object.
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

### See Also

* class [FileFontSource](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
