---
title: MemoryFontSource
second_title: Aspose.Words für .NET-API-Referenz
description: Ctor.
type: docs
weight: 10
url: /de/net/aspose.words.fonts/memoryfontsource/memoryfontsource/
---
## MemoryFontSource(byte[]) {#constructor}

Ctor.

```csharp
public MemoryFontSource(byte[] fontData)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontData | Byte[] | Binäre Schriftdaten. |

### Beispiele

Zeigt, wie ein Bytearray mit Daten aus einer Schriftartdatei als Schriftartquelle verwendet wird.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### Siehe auch

* class [MemoryFontSource](../../memoryfontsource)
* namensraum [Aspose.Words.Fonts](../../memoryfontsource)
* Montage [Aspose.Words](../../../)

---

## MemoryFontSource(byte[], int) {#constructor_1}

Ctor.

```csharp
public MemoryFontSource(byte[] fontData, int priority)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontData | Byte[] | Binäre Schriftdaten. |
| priority | Int32 | Priorität der Schriftartquelle. Siehe die[`Priority`](../../fontsourcebase/priority) Objektbeschreibung für weitere Informationen. |

### Beispiele

Zeigt, wie ein Bytearray mit Daten aus einer Schriftartdatei als Schriftartquelle verwendet wird.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### Siehe auch

* class [MemoryFontSource](../../memoryfontsource)
* namensraum [Aspose.Words.Fonts](../../memoryfontsource)
* Montage [Aspose.Words](../../../)

---

## MemoryFontSource(byte[], int, string) {#constructor_2}

Ctor.

```csharp
public MemoryFontSource(byte[] fontData, int priority, string cacheKey)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontData | Byte[] | Binäre Schriftdaten. |
| priority | Int32 | Priorität der Schriftartquelle. Siehe die[`Priority`](../../fontsourcebase/priority) Objektbeschreibung für weitere Informationen. |
| cacheKey | String | Der Schlüssel dieser Quelle im Cache. Sehen[`CacheKey`](../cachekey) Objektbeschreibung für weitere Informationen. |

### Beispiele

Zeigt, wie der Initialisierungsprozess für den Font-Cache beschleunigt wird.

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
/// Laden Sie die Schriftdaten nur bei Bedarf, anstatt sie im Speicher zu speichern
/// für die gesamte Lebensdauer des "FontSettings"-Objekts.
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

* class [MemoryFontSource](../../memoryfontsource)
* namensraum [Aspose.Words.Fonts](../../memoryfontsource)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
