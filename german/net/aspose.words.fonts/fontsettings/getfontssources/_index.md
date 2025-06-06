---
title: FontSettings.GetFontsSources
linktitle: GetFontsSources
articleTitle: GetFontsSources
second_title: Aspose.Words für .NET
description: Entdecken Sie die FontSettings GetFontsSources-Methode, um einfach auf das Quellen-Array für TrueType-Schriftarten in Aspose.Words zuzugreifen. Optimieren Sie noch heute Ihr Schriftmanagement!
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

Eine Kopie der aktuellen Schriftquellen.

## Bemerkungen

Der zurückgegebene Wert ist eine Kopie der von Aspose.Words verwendeten Daten. Änderungen an den Einträgen im zurückgegebenen Array haben keine Auswirkungen auf die Dokumentdarstellung. Um neue Schriftartenquellen anzugeben, verwenden Sie die[`SetFontsSources`](../setfontssources/) Verfahren.

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
