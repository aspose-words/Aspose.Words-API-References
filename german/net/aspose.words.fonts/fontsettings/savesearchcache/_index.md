---
title: FontSettings.SaveSearchCache
linktitle: SaveSearchCache
articleTitle: SaveSearchCache
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die SaveSearchCache-Methode von FontSettings Ihren Schriftartsuchcache effizient in einem Stream speichert und so die Leistung und das Benutzererlebnis verbessert.
type: docs
weight: 70
url: /de/net/aspose.words.fonts/fontsettings/savesearchcache/
---
## FontSettings.SaveSearchCache method

Speichert den Schriftartsuchcache im Stream.

```csharp
public void SaveSearchCache(Stream outputStream)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputStream | Stream | Ausgabestream. |

## Bemerkungen

Sehen[`SetFontsSources`](../setfontssources/) Methodenbeschreibung für weitere Informationen.

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

* class [FontSettings](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
