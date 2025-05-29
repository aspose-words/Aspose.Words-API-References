---
title: MemoryFontSource
linktitle: MemoryFontSource
articleTitle: MemoryFontSource
second_title: Aspose.Words per .NET
description: Scopri MemoryFontSource, un potente costruttore per una gestione fluida dei font nei tuoi progetti. Migliora il tuo design con facilità ed efficienza!
type: docs
weight: 10
url: /it/net/aspose.words.fonts/memoryfontsource/memoryfontsource/
---
## MemoryFontSource(*byte[]*) {#constructor}

Ctor.

```csharp
public MemoryFontSource(byte[] fontData)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontData | Byte[] | Dati binari dei font. |

## Esempi

Mostra come utilizzare un array di byte con dati provenienti da un file di font come sorgente del font.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### Guarda anche

* class [MemoryFontSource](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)

---

## MemoryFontSource(*byte[], int*) {#constructor_1}

Ctor.

```csharp
public MemoryFontSource(byte[] fontData, int priority)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontData | Byte[] | Dati binari dei font. |
| priority | Int32 | Priorità della sorgente del font. Vedi[`Priority`](../../fontsourcebase/priority/) descrizione della proprietà per maggiori informazioni. |

## Esempi

Mostra come utilizzare un array di byte con dati provenienti da un file di font come sorgente del font.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### Guarda anche

* class [MemoryFontSource](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)

---

## MemoryFontSource(*byte[], int, string*) {#constructor_2}

Ctor.

```csharp
public MemoryFontSource(byte[] fontData, int priority, string cacheKey)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontData | Byte[] | Dati binari dei font. |
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

* class [MemoryFontSource](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
