---
title: FontSettings.SetFontsFolder
second_title: Aspose.Words für .NET-API-Referenz
description: FontSettings methode. Legt den Ordner fest in dem Aspose.Words beim Rendern von Dokumenten oder beim Einbetten von Schriftarten nach TrueTypeSchriftarten sucht. Dies ist eine Verknüpfung zuSetFontsFolders zum Festlegen nur eines Schriftartenverzeichnisses.
type: docs
weight: 80
url: /de/net/aspose.words.fonts/fontsettings/setfontsfolder/
---
## FontSettings.SetFontsFolder method

Legt den Ordner fest, in dem Aspose.Words beim Rendern von Dokumenten oder beim Einbetten von Schriftarten nach TrueType-Schriftarten sucht. Dies ist eine Verknüpfung zu[`SetFontsFolders`](../setfontsfolders/) zum Festlegen nur eines Schriftartenverzeichnisses.

```csharp
public void SetFontsFolder(string fontFolder, bool recursive)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontFolder | String | Der Ordner, der TrueType-Schriftarten enthält. |
| recursive | Boolean | True, um die angegebenen Ordner rekursiv nach Schriftarten zu durchsuchen. |

### Beispiele

Zeigt, wie ein Schriftart-Quellverzeichnis festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arvo";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Unsere Schriftartquellen enthalten nicht die Schriftart, die wir für den Text in diesem Dokument verwendet haben.
// Wenn wir diese Schriftarteinstellungen beim Rendern dieses Dokuments verwenden,
// Aspose.Words wendet eine Fallback-Schriftart auf Text an, der eine Schriftart hat, die Aspose.Words nicht finden kann.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// In den Standardschriftquellen fehlen die beiden Schriftarten, die wir in diesem Dokument verwenden.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Verwenden Sie die Methode „SetFontsFolder“, um ein Verzeichnis festzulegen, das als neue Schriftartquelle fungiert.
// Übergeben Sie „false“ als „rekursives“ Argument, um Schriftarten aus allen Schriftartdateien einzuschließen, die sich im Verzeichnis befinden
// dass wir das erste Argument übergeben, aber keine Schriftarten in einem der Unterordner dieses Verzeichnisses einschließen.
// Übergeben Sie „true“ als „rekursives“ Argument, um alle Schriftartdateien in dem von uns übergebenen Verzeichnis einzuschließen
// im ersten Argument sowie alle Schriftarten in seinen Unterverzeichnissen.
FontSettings.DefaultInstance.SetFontsFolder(FontsDir, recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Die Schriftart „Amethysta“ befindet sich in einem Unterordner des Schriftartenverzeichnisses.
if (recursive)
{
    Assert.AreEqual(25, newFontSources[0].GetAvailableFonts().Count);
    Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
}
else
{
    Assert.AreEqual(18, newFontSources[0].GetAvailableFonts().Count);
    Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
}

doc.Save(ArtifactsDir + "FontSettings.SetFontsFolder.pdf");

// Die ursprünglichen Schriftartquellen wiederherstellen.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Siehe auch

* class [FontSettings](../)
* namensraum [Aspose.Words.Fonts](../../fontsettings/)
* Montage [Aspose.Words](../../../)


