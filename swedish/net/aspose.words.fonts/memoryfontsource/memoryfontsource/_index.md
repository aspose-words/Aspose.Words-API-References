---
title: MemoryFontSource.MemoryFontSource
second_title: Aspose.Words för .NET API Referens
description: MemoryFontSource byggare. Ctor.
type: docs
weight: 10
url: /sv/net/aspose.words.fonts/memoryfontsource/memoryfontsource/
---
## MemoryFontSource(byte[]) {#constructor}

Ctor.

```csharp
public MemoryFontSource(byte[] fontData)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fontData | Byte[] | Binära teckensnittsdata. |

### Exempel

Visar hur man använder en byte-array med data från en teckensnittsfil som teckensnittskälla.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### Se även

* class [MemoryFontSource](../)
* namnutrymme [Aspose.Words.Fonts](../../memoryfontsource/)
* hopsättning [Aspose.Words](../../../)

---

## MemoryFontSource(byte[], int) {#constructor_1}

Ctor.

```csharp
public MemoryFontSource(byte[] fontData, int priority)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fontData | Byte[] | Binära teckensnittsdata. |
| priority | Int32 | Teckensnittskällas prioritet. Se den[`Priority`](../../fontsourcebase/priority/) fastighetsbeskrivning för mer information. |

### Exempel

Visar hur man använder en byte-array med data från en teckensnittsfil som teckensnittskälla.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### Se även

* class [MemoryFontSource](../)
* namnutrymme [Aspose.Words.Fonts](../../memoryfontsource/)
* hopsättning [Aspose.Words](../../../)

---

## MemoryFontSource(byte[], int, string) {#constructor_2}

Ctor.

```csharp
public MemoryFontSource(byte[] fontData, int priority, string cacheKey)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fontData | Byte[] | Binära teckensnittsdata. |
| priority | Int32 | Teckensnittskällas prioritet. Se den[`Priority`](../../fontsourcebase/priority/) fastighetsbeskrivning för mer information. |
| cacheKey | String | Nyckeln till denna källa i cachen. Ser[`CacheKey`](../cachekey/) fastighetsbeskrivning för mer information. |

### Exempel

Visar hur man snabbar upp initieringsprocessen för teckensnittscache.

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
/// Ladda teckensnittsdata endast när det behövs istället för att lagra det i minnet
/// under hela livslängden för objektet "FontSettings".
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

### Se även

* class [MemoryFontSource](../)
* namnutrymme [Aspose.Words.Fonts](../../memoryfontsource/)
* hopsättning [Aspose.Words](../../../)


