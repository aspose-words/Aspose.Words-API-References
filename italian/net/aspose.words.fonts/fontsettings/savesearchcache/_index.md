---
title: FontSettings.SaveSearchCache
linktitle: SaveSearchCache
articleTitle: SaveSearchCache
second_title: Aspose.Words per .NET
description: Scopri come il metodo SaveSearchCache di FontSettings salva in modo efficiente la cache di ricerca dei font in un flusso, migliorando le prestazioni e l'esperienza utente.
type: docs
weight: 70
url: /it/net/aspose.words.fonts/fontsettings/savesearchcache/
---
## FontSettings.SaveSearchCache method

Salva la cache di ricerca dei font nel flusso.

```csharp
public void SaveSearchCache(Stream outputStream)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| outputStream | Stream | Flusso di output. |

## Osservazioni

Vedere[`SetFontsSources`](../setfontssources/) descrizione del metodo per maggiori informazioni.

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

* class [FontSettings](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
