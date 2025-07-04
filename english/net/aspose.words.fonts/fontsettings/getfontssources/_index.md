---
title: FontSettings.GetFontsSources
linktitle: GetFontsSources
articleTitle: GetFontsSources
second_title: Aspose.Words for .NET
description: Discover the FontSettings GetFontsSources method to easily access the array of sources for TrueType fonts in Aspose.Words. Optimize your font management today!
type: docs
weight: 50
url: /net/aspose.words.fonts/fontsettings/getfontssources/
---
## FontSettings.GetFontsSources method

Gets a copy of the array that contains the list of sources where Aspose.Words looks for TrueType fonts.

```csharp
public FontSourceBase[] GetFontsSources()
```

### Return Value

A copy of the current font sources.

## Remarks

The returned value is a copy of the data that Aspose.Words uses. If you change the entries in the returned array, it will have no effect on document rendering. To specify new font sources use the [`SetFontsSources`](../setfontssources/) method.

## Examples

Shows how to add a font source to our existing font sources.

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

Assert.That(originalFontSources.Length, Is.EqualTo(1));

Assert.That(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"), Is.True);

// The default font source is missing two of the fonts that we are using in our document.
// When we save this document, Aspose.Words will apply fallback fonts to all text formatted with inaccessible fonts.
Assert.That(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"), Is.False);
Assert.That(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"), Is.False);

// Create a font source from a folder that contains fonts.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Apply a new array of font sources that contains the original font sources, as well as our custom fonts.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// Verify that Aspose.Words has access to all required fonts before we render the document to PDF.
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.That(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"), Is.True);
Assert.That(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"), Is.True);
Assert.That(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"), Is.True);

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

// Restore the original font sources.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### See Also

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
