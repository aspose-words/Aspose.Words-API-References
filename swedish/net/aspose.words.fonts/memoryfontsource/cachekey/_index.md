---
title: MemoryFontSource.CacheKey
linktitle: CacheKey
articleTitle: CacheKey
second_title: Aspose.Words för .NET
description: Upptäck egenskapen MemoryFontSource CacheKey – lås upp effektiv cachning med en unik nyckel för förbättrad prestanda och optimerad minneshantering.
type: docs
weight: 20
url: /sv/net/aspose.words.fonts/memoryfontsource/cachekey/
---
## MemoryFontSource.CacheKey property

Nyckeln till denna källa i cachen.

```csharp
public string CacheKey { get; }
```

## Anmärkningar

Den här nyckeln används för att identifiera cacheobjekt när fontsökningscachen sparas/läses in med [`SaveSearchCache`](../../fontsettings/savesearchcache/) och[`SetFontsSources`](../../fontsettings/setfontssources/) metoder.

## Exempel

Visar hur man påskyndar initialiseringsprocessen för teckensnittscachen.

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
/// Ladda endast teckensnittsdata när det behövs istället för att lagra dem i minnet
/// för hela livslängden för "FontSettings"-objektet.
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

### Se även

* class [MemoryFontSource](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
