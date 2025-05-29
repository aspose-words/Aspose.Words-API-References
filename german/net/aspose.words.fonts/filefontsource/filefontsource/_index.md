---
title: FileFontSource
linktitle: FileFontSource
articleTitle: FileFontSource
second_title: Aspose.Words für .NET
description: Entdecken Sie den FileFontSource-Konstruktor für die nahtlose Schriftintegration in Ihre Projekte. Verbessern Sie Ihr Design mit benutzerfreundlichen Programmierlösungen!
type: docs
weight: 10
url: /de/net/aspose.words.fonts/filefontsource/filefontsource/
---
## FileFontSource(*string*) {#constructor}

Ctor.

```csharp
public FileFontSource(string filePath)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| filePath | String | Pfad zur Schriftartdatei. |

## Beispiele

Zeigt, wie eine Schriftartdatei im lokalen Dateisystem als Schriftartquelle verwendet wird.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### Siehe auch

* class [FileFontSource](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)

---

## FileFontSource(*string, int*) {#constructor_1}

Ctor.

```csharp
public FileFontSource(string filePath, int priority)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| filePath | String | Pfad zur Schriftartdatei. |
| priority | Int32 | Priorität der Schriftartquelle. Siehe[`Priority`](../../fontsourcebase/priority/) Weitere Informationen finden Sie in der Objektbeschreibung. |

## Beispiele

Zeigt, wie eine Schriftartdatei im lokalen Dateisystem als Schriftartquelle verwendet wird.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### Siehe auch

* class [FileFontSource](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)

---

## FileFontSource(*string, int, string*) {#constructor_2}

Ctor.

```csharp
public FileFontSource(string filePath, int priority, string cacheKey)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| filePath | String | Pfad zur Schriftartdatei. |
| priority | Int32 | Priorität der Schriftartquelle. Siehe[`Priority`](../../fontsourcebase/priority/) Weitere Informationen finden Sie in der Objektbeschreibung. |
| cacheKey | String | Der Schlüssel dieser Quelle im Cache. Siehe[`CacheKey`](../cachekey/) Weitere Informationen finden Sie in der Objektbeschreibung. |

## Beispiele

Zeigt, wie der Initialisierungsprozess des Schriftartcaches beschleunigt werden kann.

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
/// Laden Sie die Schriftdaten nur bei Bedarf, anstatt sie im Speicher zu speichern
/// für die gesamte Lebensdauer des Objekts „FontSettings“.
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

* class [FileFontSource](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
