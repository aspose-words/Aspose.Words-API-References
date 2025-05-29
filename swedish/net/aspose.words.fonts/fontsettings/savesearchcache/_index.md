---
title: FontSettings.SaveSearchCache
linktitle: SaveSearchCache
articleTitle: SaveSearchCache
second_title: Aspose.Words för .NET
description: Upptäck hur metoden FontSettings SaveSearchCache effektivt sparar din cache för teckensnittssökning till en ström, vilket förbättrar prestanda och användarupplevelse.
type: docs
weight: 70
url: /sv/net/aspose.words.fonts/fontsettings/savesearchcache/
---
## FontSettings.SaveSearchCache method

Sparar cachen för teckensnittssökning i strömmen.

```csharp
public void SaveSearchCache(Stream outputStream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| outputStream | Stream | Utgångsström. |

## Anmärkningar

Se[`SetFontsSources`](../setfontssources/) metodbeskrivning för mer information.

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

* class [FontSettings](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
