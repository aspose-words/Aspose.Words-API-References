---
title: FontSettings.SetFontsSources
linktitle: SetFontsSources
articleTitle: SetFontsSources
second_title: Aspose.Words per .NET
description: FontSettings SetFontsSources metodo. Imposta le origini in cui Aspose.Words cerca i caratteri TrueType durante il rendering di documenti o lincorporamento di caratteri in C#.
type: docs
weight: 100
url: /it/net/aspose.words.fonts/fontsettings/setfontssources/
---
## SetFontsSources(*FontSourceBase[]*) {#setfontssources}

Imposta le origini in cui Aspose.Words cerca i caratteri TrueType durante il rendering di documenti o l'incorporamento di caratteri.

```csharp
public void SetFontsSources(FontSourceBase[] sources)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sources | FontSourceBase[] | Un array di origini che contengono caratteri TrueType. |

## Osservazioni

Per impostazione predefinita, Aspose.Words cerca i caratteri installati nel sistema.

L'impostazione di questa proprietà reimposta la cache di tutti i caratteri caricati in precedenza.

## Esempi

Mostra come aggiungere una fonte di carattere alle nostre fonti di carattere esistenti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);

Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Nella fonte di carattere predefinita mancano due dei caratteri che stiamo utilizzando nel nostro documento.
// Quando salviamo questo documento, Aspose.Words applicherà i caratteri di fallback a tutto il testo formattato con caratteri inaccessibili.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Crea un'origine dei caratteri da una cartella che contiene i caratteri.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Applica una nuova serie di fonti di caratteri che contiene le fonti di caratteri originali, nonché i nostri caratteri personalizzati.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// Verifica che Aspose.Words abbia accesso a tutti i caratteri richiesti prima di eseguire il rendering del documento in PDF.
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.True(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

// Ripristina le origini dei caratteri originali.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Guarda anche

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)

---

## SetFontsSources(*FontSourceBase[], Stream*) {#setfontssources_1}

Imposta le origini in cui Aspose.Words cerca i caratteri TrueType e inoltre carica la cache di ricerca dei caratteri precedentemente salvata .

```csharp
public void SetFontsSources(FontSourceBase[] sources, Stream cacheInputStream)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sources | FontSourceBase[] | Un array di origini che contengono caratteri TrueType. |
| cacheInputStream | Stream | Flusso di input con cache di ricerca dei caratteri salvata. |

## Osservazioni

Il caricamento della cache di ricerca dei caratteri salvata in precedenza accelererà il processo di inizializzazione della cache dei caratteri. È particolarmente utile quando l'accesso alle fonti dei caratteri è complicato (ad esempio quando i caratteri vengono caricati tramite rete).

Durante il salvataggio e il caricamento della cache di ricerca dei caratteri, i caratteri nelle origini fornite vengono identificati tramite la chiave cache. Per i caratteri nella[`SystemFontSource`](../../systemfontsource/) E[`FolderFontSource`](../../folderfontsource/) la chiave della cache è il percorso del file del carattere. Per[`MemoryFontSource`](../../memoryfontsource/) E[`StreamFontSource`](../../streamfontsource/) la chiave della cache è definita nel file[`CacheKey`](../../memoryfontsource/cachekey/) E[`CacheKey`](../../streamfontsource/cachekey/) proprietà rispettivamente. Per il[`FileFontSource`](../../filefontsource/) la chiave della cache è uno dei due[`CacheKey`](../../filefontsource/cachekey/) o un percorso file se il file[`CacheKey`](../../filefontsource/cachekey/) È`nullo`.

Si consiglia vivamente di fornire le stesse origini dei caratteri durante il caricamento della cache come al momento del salvataggio della cache. Eventuali modifiche alle origini dei caratteri (ad esempio l'aggiunta di nuovi caratteri, lo spostamento di file di caratteri o la modifica della chiave della cache) possono portare a caratteri imprecisi risolvendo da Aspose.Words.

## Esempi

Mostra come velocizzare il processo di inizializzazione della cache dei caratteri.

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
/// Carica i dati dei caratteri solo quando richiesto invece di archiviarli nella memoria
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

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
