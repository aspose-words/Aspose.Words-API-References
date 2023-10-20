---
title: FontSettings.GetFontsSources
linktitle: GetFontsSources
articleTitle: GetFontsSources
second_title: Aspose.Words für .NET
description: FontSettings GetFontsSources methode. Ruft eine Kopie des Arrays ab das die Liste der Quellen enthält in denen Aspose.Words nach TrueTypeSchriftarten sucht in C#.
type: docs
weight: 50
url: /de/net/aspose.words.fonts/fontsettings/getfontssources/
---
## FontSettings.GetFontsSources method

Ruft eine Kopie des Arrays ab, das die Liste der Quellen enthält, in denen Aspose.Words nach TrueType-Schriftarten sucht.

```csharp
public FontSourceBase[] GetFontsSources()
```

### Rückgabewert

Eine Kopie der aktuellen Schriftartquellen.

## Bemerkungen

Der zurückgegebene Wert ist eine Kopie der Daten, die Aspose.Words verwendet. Wenn Sie die Einträge im zurückgegebenen Array ändern, hat dies keine Auswirkungen auf die Dokumentwiedergabe. Um neue Schriftarten anzugeben, verwenden Sie „sources “.[`SetFontsSources`](../setfontssources/) Methode.

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
