---
title: FontSettings.SetFontsSources
linktitle: SetFontsSources
articleTitle: SetFontsSources
second_title: Aspose.Words per .NET
description: Scopri come il metodo SetFontsSources in Aspose.Words migliora il rendering dei documenti specificando le origini dei font TrueType per risultati ottimali.
type: docs
weight: 100
url: /it/net/aspose.words.fonts/fontsettings/setfontssources/
---
## SetFontsSources(*FontSourceBase[]*) {#setfontssources}

Imposta le origini in cui Aspose.Words cerca i font TrueType durante il rendering dei documenti o l'incorporamento dei font.

```csharp
public void SetFontsSources(FontSourceBase[] sources)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sources | FontSourceBase[] | Una serie di fonti che contengono font TrueType. |

## Osservazioni

Per impostazione predefinita, Aspose.Words cerca i font installati nel sistema.

Impostando questa proprietà si reimposta la cache di tutti i font caricati in precedenza.

## Esempi

Mostra come aggiungere una sorgente font alle nostre sorgenti font esistenti.

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

// Nella sorgente font predefinita mancano due dei font che stiamo utilizzando nel nostro documento.
// Quando salviamo questo documento, Aspose.Words applicherà font di fallback a tutto il testo formattato con font inaccessibili.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Crea una sorgente font da una cartella che contiene font.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Applica un nuovo array di sorgenti di font che contiene le sorgenti di font originali, nonché i nostri font personalizzati.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// Verificare che Aspose.Words abbia accesso a tutti i font richiesti prima di convertire il documento in PDF.
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.True(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

// Ripristina le sorgenti dei font originali.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Guarda anche

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)

---

## SetFontsSources(*FontSourceBase[], Stream*) {#setfontssources_1}

Imposta le origini in cui Aspose.Words cerca i font TrueType e carica inoltre la cache di ricerca dei font salvata in precedenza .

```csharp
public void SetFontsSources(FontSourceBase[] sources, Stream cacheInputStream)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sources | FontSourceBase[] | Una serie di fonti che contengono font TrueType. |
| cacheInputStream | Stream | Flusso di input con cache di ricerca dei font salvata. |

## Osservazioni

Il caricamento della cache di ricerca dei font salvata in precedenza velocizzerà il processo di inizializzazione della cache. È particolarmente utile quando l'accesso alle fonti dei font è complicato (ad esempio quando i font vengono caricati tramite rete).

Durante il salvataggio e il caricamento della cache di ricerca dei font, i font nelle fonti fornite vengono identificati tramite la chiave cache. Per i font nella[`SystemFontSource`](../../systemfontsource/) E[`FolderFontSource`](../../folderfontsource/) la chiave della cache è il percorso al file del font. Per[`MemoryFontSource`](../../memoryfontsource/) E[`StreamFontSource`](../../streamfontsource/)la chiave della cache è definita in[`CacheKey`](../../memoryfontsource/cachekey/) E[`CacheKey`](../../streamfontsource/cachekey/) properties rispettivamente. Per il[`FileFontSource`](../../filefontsource/) la chiave della cache è[`CacheKey`](../../filefontsource/cachekey/) Proprietà o un percorso di file se[`CacheKey`](../../filefontsource/cachekey/) È`null`.

Si consiglia vivamente di fornire le stesse sorgenti dei font quando si carica la cache, come al momento del salvataggio della cache. Qualsiasi modifica alle sorgenti dei font (ad esempio l'aggiunta di nuovi font, lo spostamento dei file di font o la modifica della chiave della cache) potrebbe causare una risoluzione dei font imprecisa da parte di Aspose.Words.

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

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
