---
title: FontSettings.SetFontsFolder
linktitle: SetFontsFolder
articleTitle: SetFontsFolder
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit der Methode SetFontsFolder ein TrueType-Schriftartenverzeichnis in Aspose.Words angeben und so die Dokumentwiedergabe und Schriftarteneinbettung verbessern.
type: docs
weight: 80
url: /de/net/aspose.words.fonts/fontsettings/setfontsfolder/
---
## FontSettings.SetFontsFolder method

Legt den Ordner fest, in dem Aspose.Words beim Rendern von Dokumenten oder beim Einbetten von Schriftarten nach TrueType-Schriftarten sucht. Dies ist eine Verknüpfung zu[`SetFontsFolders`](../setfontsfolders/) zum Einstellen nur eines Schriftartenverzeichnisses.

```csharp
public void SetFontsFolder(string fontFolder, bool recursive)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontFolder | String | Der Ordner, der TrueType-Schriftarten enthält. |
| recursive | Boolean | True, um die angegebenen Ordner rekursiv nach Schriftarten zu durchsuchen. |

## Beispiele

Zeigt, wie ein Schriftartquellenverzeichnis festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arvo";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Unsere Schriftartquellen enthalten nicht die Schriftart, die wir für den Text in diesem Dokument verwendet haben.
// Wenn wir diese Schrifteinstellungen beim Rendern dieses Dokuments verwenden,
// Aspose.Words wendet eine Ersatzschriftart auf Text an, der eine Schriftart enthält, die Aspose.Words nicht finden kann.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// In den Standardschriftartenquellen fehlen die beiden Schriftarten, die wir in diesem Dokument verwenden.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Verwenden Sie die Methode „SetFontsFolder“, um ein Verzeichnis festzulegen, das als neue Schriftartquelle fungiert.
// Übergeben Sie "false" als "rekursives" Argument, um Schriftarten aus allen Schriftartdateien einzuschließen, die sich im Verzeichnis befinden
// dass wir das erste Argument übergeben, aber keine Schriftarten in den Unterordnern dieses Verzeichnisses einschließen.
// Übergeben Sie "true" als "rekursives" Argument, um alle Schriftdateien im Verzeichnis einzuschließen, das wir übergeben
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

// Stellen Sie die ursprünglichen Schriftartquellen wieder her.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Siehe auch

* class [FontSettings](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
