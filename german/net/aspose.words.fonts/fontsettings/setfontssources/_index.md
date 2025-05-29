---
title: FontSettings.SetFontsSources
linktitle: SetFontsSources
articleTitle: SetFontsSources
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Methode SetFontsSources in Aspose.Words die Dokumentwiedergabe verbessert, indem sie TrueType-Schriftquellen für optimale Ergebnisse angibt.
type: docs
weight: 100
url: /de/net/aspose.words.fonts/fontsettings/setfontssources/
---
## SetFontsSources(*FontSourceBase[]*) {#setfontssources}

Legt die Quellen fest, in denen Aspose.Words beim Rendern von Dokumenten oder beim Einbetten von Schriftarten nach TrueType-Schriftarten sucht.

```csharp
public void SetFontsSources(FontSourceBase[] sources)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sources | FontSourceBase[] | Ein Array von Quellen, die TrueType-Schriftarten enthalten. |

## Bemerkungen

Standardmäßig sucht Aspose.Words nach auf dem System installierten Schriftarten.

Durch Festlegen dieser Eigenschaft wird der Cache aller zuvor geladenen Schriftarten zurückgesetzt.

## Beispiele

Zeigt, wie wir unseren vorhandenen Schriftartquellen eine Schriftartquelle hinzufügen.

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

// In der Standardschriftartquelle fehlen zwei der Schriftarten, die wir in unserem Dokument verwenden.
// Wenn wir dieses Dokument speichern, wendet Aspose.Words Ersatzschriftarten auf den gesamten Text an, der mit nicht zugänglichen Schriftarten formatiert ist.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Erstellen Sie eine Schriftartquelle aus einem Ordner, der Schriftarten enthält.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Wenden Sie ein neues Array von Schriftartquellen an, das die ursprünglichen Schriftartquellen sowie unsere benutzerdefinierten Schriftarten enthält.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// Überprüfen Sie, ob Aspose.Words Zugriff auf alle erforderlichen Schriftarten hat, bevor wir das Dokument in PDF rendern.
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
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)

---

## SetFontsSources(*FontSourceBase[], Stream*) {#setfontssources_1}

Legt die Quellen fest, in denen Aspose.Words nach TrueType-Schriftarten sucht und lädt zusätzlich zuvor gespeicherte Schriftartensuch-Cache.

```csharp
public void SetFontsSources(FontSourceBase[] sources, Stream cacheInputStream)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sources | FontSourceBase[] | Ein Array von Quellen, die TrueType-Schriftarten enthalten. |
| cacheInputStream | Stream | Eingabestream mit gespeichertem Schriftartensuchcache. |

## Bemerkungen

Das Laden eines zuvor gespeicherten Font-Suchcaches beschleunigt die Initialisierung des Font-Caches. Dies ist besonders nützlich, wenn der Zugriff auf Fontquellen kompliziert ist (z. B. wenn Fonts über das Netzwerk geladen werden).

Beim Speichern und Laden des Font-Such-Cache werden die Fonts in den bereitgestellten Quellen über den Cache-Schlüssel identifiziert. Für die Fonts im[`SystemFontSource`](../../systemfontsource/) Und[`FolderFontSource`](../../folderfontsource/) Cache-Schlüssel ist der Pfad zur Schriftartdatei. Für[`MemoryFontSource`](../../memoryfontsource/) Und[`StreamFontSource`](../../streamfontsource/)Cache-Schlüssel ist definiert in der[`CacheKey`](../../memoryfontsource/cachekey/) Und[`CacheKey`](../../streamfontsource/cachekey/) properties bzw. Für die[`FileFontSource`](../../filefontsource/) Cache-Schlüssel ist entweder[`CacheKey`](../../filefontsource/cachekey/) -Eigenschaft oder ein Dateipfad, wenn die[`CacheKey`](../../filefontsource/cachekey/) Ist`null`.

Es wird dringend empfohlen, beim Laden des Caches dieselben Schriftartquellen anzugeben wie zum Zeitpunkt der Speicherung des Caches. Jegliche Änderungen an den Schriftartquellen (z. B. Hinzufügen neuer Schriftarten, Verschieben von Schriftartdateien oder Ändern des Cache-Schlüssels) können zu einer ungenauen Schriftartauflösung durch Aspose.Words führen.

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

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
