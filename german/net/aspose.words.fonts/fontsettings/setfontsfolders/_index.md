---
title: FontSettings.SetFontsFolders
linktitle: SetFontsFolders
articleTitle: SetFontsFolders
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit der Methode SetFontsFolders in Aspose.Words die Speicherorte von TrueType-Schriftarten für eine optimale Dokumentwiedergabe und -einbettung anpassen.
type: docs
weight: 90
url: /de/net/aspose.words.fonts/fontsettings/setfontsfolders/
---
## FontSettings.SetFontsFolders method

Legt die Ordner fest, in denen Aspose.Words beim Rendern von Dokumenten oder beim Einbetten von Schriftarten nach TrueType-Schriftarten sucht.

```csharp
public void SetFontsFolders(string[] fontsFolders, bool recursive)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontsFolders | String[] | Ein Array von Ordnern, die TrueType-Schriftarten enthalten. |
| recursive | Boolean | True, um die angegebenen Ordner rekursiv nach Schriftarten zu durchsuchen. |

## Bemerkungen

Standardmäßig sucht Aspose.Words nach auf dem System installierten Schriftarten.

Durch Festlegen dieser Eigenschaft wird der Cache aller zuvor geladenen Schriftarten zurückgesetzt.

## Beispiele

Zeigt, wie mehrere Schriftartquellenverzeichnisse festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Unsere Schriftartquellen enthalten nicht die Schriftart, die wir für den Text in diesem Dokument verwendet haben.
// Wenn wir diese Schrifteinstellungen beim Rendern dieses Dokuments verwenden,
// Aspose.Words wendet eine Ersatzschriftart auf Text an, der eine Schriftart enthält, die Aspose.Words nicht finden kann.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// In den Standardschriftartenquellen fehlen die beiden Schriftarten, die wir in diesem Dokument verwenden.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Verwenden Sie die Methode „SetFontsFolders“, um aus jedem Schriftartenverzeichnis, das wir als erstes Argument übergeben, eine Schriftartenquelle zu erstellen.
// Übergeben Sie "false" als "rekursives" Argument, um Schriftarten aus allen Schriftartdateien einzuschließen, die sich in den Verzeichnissen befinden
// die wir im ersten Argument übergeben, aber keine Schriftarten aus den Unterordnern der Verzeichnisse einschließen.
// Übergeben Sie "true" als "rekursives" Argument, um alle Schriftdateien in den Verzeichnissen einzuschließen, die wir übergeben
// im ersten Argument sowie alle Schriftarten in ihren Unterverzeichnissen.
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Der Ordner „Junction“ selbst enthält keine Schriftdateien, hat aber Unterordner, die welche enthalten.
if (recursive)
{
    Assert.AreEqual(6, newFontSources[1].GetAvailableFonts().Count);
    Assert.True(newFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));
}
else
{
    Assert.AreEqual(0, newFontSources[1].GetAvailableFonts().Count);
}

doc.Save(ArtifactsDir + "FontSettings.SetFontsFolders.pdf");

// Stellen Sie die ursprünglichen Schriftartquellen wieder her.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Siehe auch

* class [FontSettings](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
