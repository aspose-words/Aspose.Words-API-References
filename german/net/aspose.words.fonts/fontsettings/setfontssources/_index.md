---
title: FontSettings.SetFontsSources
linktitle: SetFontsSources
articleTitle: SetFontsSources
second_title: Aspose.Words für .NET
description: FontSettings SetFontsSources methode. Legt die Quellen fest in denen Aspose.Words beim Rendern von Dokumenten oder beim Einbetten von Schriftarten nach TrueTypeSchriftarten sucht in C#.
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

Durch das Festlegen dieser Eigenschaft wird der Cache aller zuvor geladenen Schriftarten zurückgesetzt.

## Beispiele

Zeigt, wie Sie eine Schriftartenquelle zu unseren vorhandenen Schriftartenquellen hinzufügen.

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

// Der Standardschriftquelle fehlen zwei der Schriftarten, die wir in unserem Dokument verwenden.
// Wenn wir dieses Dokument speichern, wendet Aspose.Words Fallback-Schriftarten auf den gesamten Text an, der mit nicht zugänglichen Schriftarten formatiert ist.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Erstelle eine Schriftartenquelle aus einem Ordner, der Schriftarten enthält.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Anwenden eines neuen Arrays von Schriftartquellen, das die ursprünglichen Schriftartquellen sowie unsere benutzerdefinierten Schriftarten enthält.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// Stellen Sie sicher, dass Aspose.Words Zugriff auf alle erforderlichen Schriftarten hat, bevor wir das Dokument in PDF rendern.
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.True(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

// Die ursprünglichen Schriftartquellen wiederherstellen.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Siehe auch

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)

---

## SetFontsSources(*FontSourceBase[], Stream*) {#setfontssources_1}

Legt die Quellen fest, in denen Aspose.Words nach TrueType-Schriftarten sucht, und lädt zusätzlich den zuvor gespeicherten Schriftarten-Suchcache.

```csharp
public void SetFontsSources(FontSourceBase[] sources, Stream cacheInputStream)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sources | FontSourceBase[] | Ein Array von Quellen, die TrueType-Schriftarten enthalten. |
| cacheInputStream | Stream | Eingabestream mit gespeichertem Cache für die Schriftartensuche. |

## Bemerkungen

Das Laden eines zuvor gespeicherten Schriftarten-Suchcaches beschleunigt den Initialisierungsprozess des Schriftarten-Caches. Dies ist besonders nützlich, wenn der Zugriff auf Schriftartquellen kompliziert ist (z. B. wenn Schriftarten über das Netzwerk geladen werden).

Beim Speichern und Laden des Schriftarten-Suchcaches werden Schriftarten in den bereitgestellten Quellen über den Cache-Schlüssel identifiziert. Für die Schriftarten im[`SystemFontSource`](../../systemfontsource/) Und[`FolderFontSource`](../../folderfontsource/) Der Cache-Schlüssel ist der Pfad zur Schriftartendatei. Für[`MemoryFontSource`](../../memoryfontsource/) Und[`StreamFontSource`](../../streamfontsource/) Der Cache-Schlüssel ist definiert im[`CacheKey`](../../memoryfontsource/cachekey/) Und[`CacheKey`](../../streamfontsource/cachekey/) Properties bzw. Für die[`FileFontSource`](../../filefontsource/) Cache-Schlüssel ist entweder[`CacheKey`](../../filefontsource/cachekey/) -Eigenschaft oder einen Dateipfad, wenn die[`CacheKey`](../../filefontsource/cachekey/) Ist`Null`.

Es wird dringend empfohlen, beim Laden des Caches dieselben Schriftartenquellen bereitzustellen wie zum Zeitpunkt des Speicherns des Caches. Alle Änderungen an den Schriftartenquellen (z. B. das Hinzufügen neuer Schriftarten, das Verschieben von Schriftartendateien oder das Ändern des Cache-Schlüssels) können dazu führen, dass die Schriftart ungenau ist Auflösung durch Aspose.Words.

## Beispiele

Zeigt, wie der Initialisierungsprozess für den Schriftcache beschleunigt werden kann.

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
/// Laden Sie die Schriftartdaten nur bei Bedarf, anstatt sie im Speicher zu speichern
/// für die gesamte Lebensdauer des „FontSettings“-Objekts.
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
