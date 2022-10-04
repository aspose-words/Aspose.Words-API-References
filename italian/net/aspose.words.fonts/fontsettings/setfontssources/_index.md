---
title: SetFontsSources
second_title: Aspose.Words per .NET API Reference
description: Imposta le origini in cui Aspose.Words cerca i caratteri TrueType durante il rendering di documenti o lincorporamento di caratteri.
type: docs
weight: 100
url: /it/net/aspose.words.fonts/fontsettings/setfontssources/
---
## SetFontsSources(FontSourceBase[]) {#setfontssources}

Imposta le origini in cui Aspose.Words cerca i caratteri TrueType durante il rendering di documenti o l'incorporamento di caratteri.

```csharp
public void SetFontsSources(FontSourceBase[] sources)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sources | FontSourceBase[] | Una matrice di sorgenti che contengono caratteri TrueType. |

### Osservazioni

Per impostazione predefinita, Aspose.Words cerca i font installati nel sistema.

L'impostazione di questa proprietà reimposta la cache di tutti i caratteri caricati in precedenza.

### Esempi

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

// L'origine dei caratteri predefinita manca di due dei caratteri che stiamo utilizzando nel nostro documento.
// Quando salviamo questo documento, Aspose.Words applicherà i caratteri di fallback a tutto il testo formattato con caratteri inaccessibili.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Crea una fonte di font da una cartella che contiene font.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Applica una nuova matrice di fonti di carattere che contiene le fonti di carattere originali, oltre ai nostri caratteri personalizzati.
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
* spazio dei nomi [Aspose.Words.Fonts](../../fontsettings/)
* assemblea [Aspose.Words](../../../)

---

## SetFontsSources(FontSourceBase[], Stream) {#setfontssources_1}

Imposta le origini in cui Aspose.Words cerca i caratteri TrueType e carica inoltre la cache di ricerca dei caratteri precedentemente salvata .

```csharp
public void SetFontsSources(FontSourceBase[] sources, Stream cacheInputStream)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sources | FontSourceBase[] | Una matrice di sorgenti che contengono caratteri TrueType. |
| cacheInputStream | Stream | Flusso di input con la cache di ricerca dei caratteri salvata. |

### Osservazioni

Il caricamento della cache di ricerca dei font salvata in precedenza accelererà il processo di inizializzazione della cache dei font. È particolarmente utile quando l'accesso alle fonti dei caratteri è complicato (ad esempio quando i caratteri vengono caricati tramite rete).

Quando si salva e si carica la cache di ricerca dei caratteri, i caratteri nelle fonti fornite vengono identificati tramite la chiave della cache. Per i caratteri nella[`SystemFontSource`](../../systemfontsource/) e[`FolderFontSource`](../../folderfontsource/) la chiave della cache è il percorso del file del carattere. Per[`MemoryFontSource`](../../memoryfontsource/) e[`StreamFontSource`](../../streamfontsource/) la chiave della cache è definita nel file[`CacheKey`](../../memoryfontsource/cachekey/) e[`CacheKey`](../../streamfontsource/cachekey/) properties rispettivamente. Per il[`FileFontSource`](../../filefontsource/) la chiave della cache è sia[`CacheKey`](../../filefontsource/cachekey/) o un percorso di file se il[`CacheKey`](../../filefontsource/cachekey/) è **nullo**.

Si consiglia vivamente di fornire le stesse origini dei caratteri durante il caricamento della cache del momento in cui la cache è stata salvata. Eventuali modifiche alle origini dei caratteri (ad esempio l'aggiunta di nuovi caratteri, lo spostamento di file di caratteri o la modifica della chiave della cache) possono comportare un carattere impreciso del risoluzione di Aspose.Words.

### Esempi

Mostra come accelerare il processo di inizializzazione della cache dei caratteri.

```csharp
[Test]
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
/// Carica i dati del font solo quando richiesto invece di salvarli in memoria
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
* spazio dei nomi [Aspose.Words.Fonts](../../fontsettings/)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
