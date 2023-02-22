---
title: FontSettings.SetFontsSources
second_title: Aspose.Words für .NET-API-Referenz
description: FontSettings methode. Legt die Quellen fest in denen Aspose.Words beim Rendern von Dokumenten oder beim Einbetten von Schriftarten nach TrueTypeSchriftarten sucht.
type: docs
weight: 100
url: /de/net/aspose.words.fonts/fontsettings/setfontssources/
---
## SetFontsSources(FontSourceBase[]) {#setfontssources}

Legt die Quellen fest, in denen Aspose.Words beim Rendern von Dokumenten oder beim Einbetten von Schriftarten nach TrueType-Schriftarten sucht.

```csharp
public void SetFontsSources(FontSourceBase[] sources)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sources | FontSourceBase[] | Ein Array von Quellen, die TrueType-Schriftarten enthalten. |

### Bemerkungen

Standardmäßig sucht Aspose.Words nach auf dem System installierten Schriftarten.

Wenn Sie diese Eigenschaft festlegen, wird der Cache aller zuvor geladenen Schriftarten zurückgesetzt.

### Beispiele

Zeigt, wie eine Schriftartquelle zu unseren vorhandenen Schriftartquellen hinzugefügt wird.

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

// Der Standard-Schriftquelle fehlen zwei der Schriftarten, die wir in unserem Dokument verwenden.
// Wenn wir dieses Dokument speichern, wendet Aspose.Words Fallback-Schriftarten auf allen Text an, der mit nicht zugänglichen Schriftarten formatiert ist.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Erstellen Sie eine Schriftartquelle aus einem Ordner, der Schriftarten enthält.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Wenden Sie ein neues Array von Schriftartquellen an, das die ursprünglichen Schriftartquellen sowie unsere benutzerdefinierten Schriftarten enthält.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// Stellen Sie sicher, dass Aspose.Words Zugriff auf alle erforderlichen Schriftarten hat, bevor wir das Dokument als PDF rendern.
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.True(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

// Stellen Sie die ursprünglichen Schriftartquellen wieder her.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Siehe auch

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* namensraum [Aspose.Words.Fonts](../../fontsettings/)
* Montage [Aspose.Words](../../../)

---

## SetFontsSources(FontSourceBase[], Stream) {#setfontssources_1}

Legt die Quellen fest, in denen Aspose.Words nach TrueType-Schriftarten sucht und lädt zusätzlich zuvor gespeicherte Schriftsuchcache.

```csharp
public void SetFontsSources(FontSourceBase[] sources, Stream cacheInputStream)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sources | FontSourceBase[] | Ein Array von Quellen, die TrueType-Schriftarten enthalten. |
| cacheInputStream | Stream | Eingabestream mit gespeichertem Fontsuchcache. |

### Bemerkungen

Das Laden eines zuvor gespeicherten Font-Such-Cache beschleunigt den Initialisierungsprozess des Font-Cache. Es ist besonders nützlich, wenn der Zugriff auf Fontquellen kompliziert ist (z. B. wenn Fonts über das Netzwerk geladen werden).

Beim Speichern und Laden des Font-Such-Cache werden Fonts in den bereitgestellten Quellen über den Cache-Schlüssel identifiziert. Für die Fonts im[`SystemFontSource`](../../systemfontsource/) und[`FolderFontSource`](../../folderfontsource/) Cache-Schlüssel ist der Pfad zur Schriftartdatei. Zum[`MemoryFontSource`](../../memoryfontsource/) und[`StreamFontSource`](../../streamfontsource/) Cache-Schlüssel ist defined in der[`CacheKey`](../../memoryfontsource/cachekey/) und[`CacheKey`](../../streamfontsource/cachekey/) properties bzw. Für die[`FileFontSource`](../../filefontsource/) Cache-Schlüssel ist entweder[`CacheKey`](../../filefontsource/cachekey/) -Eigenschaft oder ein Dateipfad, wenn die[`CacheKey`](../../filefontsource/cachekey/) ist **Null**.

Es wird dringend empfohlen, beim Laden des Caches dieselben Schriftquellen bereitzustellen wie zum Zeitpunkt des Speicherns des Caches. Jegliche Änderungen an den Schriftquellen (z. B. Hinzufügen neuer Schriftarten, Verschieben von Schriftdateien oder Ändern des Cache-Schlüssels) können zu einer ungenauen Schriftart der führen Auflösung durch Aspose.Words.

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

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* namensraum [Aspose.Words.Fonts](../../fontsettings/)
* Montage [Aspose.Words](../../../)


