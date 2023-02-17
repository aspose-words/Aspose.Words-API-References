---
title: FileFontSource.FileFontSource
second_title: Aspose.Words for .NET API Reference
description: FileFontSource constructor. Ctor in C#.
type: docs
weight: 10
url: /net/aspose.words.fonts/filefontsource/filefontsource/
---
## FileFontSource(string) {#constructor}

Ctor.

```csharp
public FileFontSource(string filePath)
```

| Parameter | Type | Description |
| --- | --- | --- |
| filePath | String | Path to font file. |

## Examples

Shows how to use a font file in the local file system as a font source.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### See Also

* class [FileFontSource](../)
* namespace [Aspose.Words.Fonts](../../filefontsource/)
* assembly [Aspose.Words](../../../)

---

## FileFontSource(string, int) {#constructor_1}

Ctor.

```csharp
public FileFontSource(string filePath, int priority)
```

| Parameter | Type | Description |
| --- | --- | --- |
| filePath | String | Path to font file. |
| priority | Int32 | Font source priority. See the [`Priority`](../../fontsourcebase/priority/) property description for more information. |

## Examples

Shows how to use a font file in the local file system as a font source.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### See Also

* class [FileFontSource](../)
* namespace [Aspose.Words.Fonts](../../filefontsource/)
* assembly [Aspose.Words](../../../)

---

## FileFontSource(string, int, string) {#constructor_2}

Ctor.

```csharp
public FileFontSource(string filePath, int priority, string cacheKey)
```

| Parameter | Type | Description |
| --- | --- | --- |
| filePath | String | Path to font file. |
| priority | Int32 | Font source priority. See the [`Priority`](../../fontsourcebase/priority/) property description for more information. |
| cacheKey | String | The key of this source in the cache. See [`CacheKey`](../cachekey/) property description for more information. |

## Examples

Shows how to speed up the font cache initialization process.

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
/// Load the font data only when required instead of storing it in the memory
/// for the entire lifetime of the "FontSettings" object.
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

### See Also

* class [FileFontSource](../)
* namespace [Aspose.Words.Fonts](../../filefontsource/)
* assembly [Aspose.Words](../../../)
