---
title: MemoryFontSource.CacheKey
linktitle: CacheKey
articleTitle: CacheKey
second_title: Aspose.Words für .NET
description: Entdecken Sie die CacheKey-Eigenschaft von MemoryFontSource – entsperren Sie effizientes Caching mit einem eindeutigen Schlüssel für verbesserte Leistung und optimierte Speicherverwaltung.
type: docs
weight: 20
url: /de/net/aspose.words.fonts/memoryfontsource/cachekey/
---
## MemoryFontSource.CacheKey property

Der Schlüssel dieser Quelle im Cache.

```csharp
public string CacheKey { get; }
```

## Bemerkungen

Dieser Schlüssel wird verwendet, um Cache-Elemente beim Speichern/Laden des Schriftartensuchcaches mit zu identifizieren.[`SaveSearchCache`](../../fontsettings/savesearchcache/) Und[`SetFontsSources`](../../fontsettings/setfontssources/) Methoden.

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

* class [MemoryFontSource](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
