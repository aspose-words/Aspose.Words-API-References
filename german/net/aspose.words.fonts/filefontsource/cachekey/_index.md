---
title: FileFontSource.CacheKey
linktitle: CacheKey
articleTitle: CacheKey
second_title: Aspose.Words für .NET
description: Entdecken Sie die FileFontSource CacheKey-Eigenschaft, Ihren Schlüssel zu effizienter Schriftartverwaltung und optimiertem Caching für verbesserte Leistung.
type: docs
weight: 20
url: /de/net/aspose.words.fonts/filefontsource/cachekey/
---
## FileFontSource.CacheKey property

Der Schlüssel dieser Quelle im Cache.

```csharp
public string CacheKey { get; }
```

## Bemerkungen

Dieser Schlüssel wird verwendet, um Cache-Elemente beim Speichern/Laden des Schriftartensuchcaches mit zu identifizieren[`SaveSearchCache`](../../fontsettings/savesearchcache/) und [`SetFontsSources`](../../fontsettings/setfontssources/) Methoden.

Wenn kein Schlüssel angegeben ist, dann[`FilePath`](../filepath/) wird stattdessen als Schlüssel verwendet.

## Beispiele

Zeigt, wie der Initialisierungsprozess des Schriftartcaches beschleunigt werden kann.

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
/// Laden Sie die Schriftdaten nur bei Bedarf, anstatt sie im Speicher zu speichern
/// für die gesamte Lebensdauer des Objekts „FontSettings“.
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

### Siehe auch

* class [FileFontSource](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
