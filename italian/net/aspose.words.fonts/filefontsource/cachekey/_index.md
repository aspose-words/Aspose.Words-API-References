---
title: FileFontSource.CacheKey
linktitle: CacheKey
articleTitle: CacheKey
second_title: Aspose.Words per .NET
description: Scopri la proprietà CacheKey di FileFontSource, la chiave per una gestione efficiente dei font e una memorizzazione nella cache ottimizzata per prestazioni migliorate.
type: docs
weight: 20
url: /it/net/aspose.words.fonts/filefontsource/cachekey/
---
## FileFontSource.CacheKey property

La chiave di questa sorgente nella cache.

```csharp
public string CacheKey { get; }
```

## Osservazioni

Questa chiave viene utilizzata per identificare l'elemento della cache durante il salvataggio/caricamento della cache di ricerca dei font con [`SaveSearchCache`](../../fontsettings/savesearchcache/) e [`SetFontsSources`](../../fontsettings/setfontssources/) metodi.

Se la chiave non è specificata allora[`FilePath`](../filepath/) verrà utilizzato come chiave.

## Esempi

Mostra come velocizzare il processo di inizializzazione della cache dei font.

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
/// Carica i dati del font solo quando necessario invece di memorizzarli nella memoria
/// per l'intera durata dell'oggetto "FontSettings".
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

### Guarda anche

* class [FileFontSource](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
