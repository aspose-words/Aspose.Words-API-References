---
title: FileFontSource
linktitle: FileFontSource
articleTitle: FileFontSource
second_title: Aspose.Words per .NET
description: Scopri il costruttore FileFontSource per un'integrazione perfetta dei font nei tuoi progetti. Migliora il tuo design con soluzioni di programmazione facili da usare!
type: docs
weight: 10
url: /it/net/aspose.words.fonts/filefontsource/filefontsource/
---
## FileFontSource(*string*) {#constructor}

Ctor.

```csharp
public FileFontSource(string filePath)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| filePath | String | Percorso al file del font. |

## Esempi

Mostra come utilizzare un file di font nel file system locale come origine del font.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### Guarda anche

* class [FileFontSource](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)

---

## FileFontSource(*string, int*) {#constructor_1}

Ctor.

```csharp
public FileFontSource(string filePath, int priority)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| filePath | String | Percorso al file del font. |
| priority | Int32 | Priorità della sorgente del font. Vedi[`Priority`](../../fontsourcebase/priority/) descrizione della proprietà per maggiori informazioni. |

## Esempi

Mostra come utilizzare un file di font nel file system locale come origine del font.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### Guarda anche

* class [FileFontSource](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)

---

## FileFontSource(*string, int, string*) {#constructor_2}

Ctor.

```csharp
public FileFontSource(string filePath, int priority, string cacheKey)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| filePath | String | Percorso al file del font. |
| priority | Int32 | Priorità della sorgente del font. Vedi[`Priority`](../../fontsourcebase/priority/) descrizione della proprietà per maggiori informazioni. |
| cacheKey | String | La chiave di questa fonte nella cache. Vedi[`CacheKey`](../cachekey/) descrizione della proprietà per maggiori informazioni. |

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
