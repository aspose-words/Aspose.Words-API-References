---
title: FontSettings.SetFontsFolder
linktitle: SetFontsFolder
articleTitle: SetFontsFolder
second_title: Aspose.Words for .NET
description: Discover how to use the SetFontsFolder method to specify a TrueType font directory in Aspose.Words, enhancing document rendering and font embedding.
type: docs
weight: 80
url: /net/aspose.words.fonts/fontsettings/setfontsfolder/
---
## FontSettings.SetFontsFolder method

Sets the folder where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts. This is a shortcut to [`SetFontsFolders`](../setfontsfolders/) for setting only one font directory.

```csharp
public void SetFontsFolder(string fontFolder, bool recursive)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fontFolder | String | The folder that contains TrueType fonts. |
| recursive | Boolean | True to scan the specified folders for fonts recursively. |

## Examples

Shows how to set a font source directory.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arvo";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Our font sources do not contain the font that we have used for text in this document.
// If we use these font settings while rendering this document,
// Aspose.Words will apply a fallback font to text which has a font that Aspose.Words cannot locate.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.That(originalFontSources.Length, Is.EqualTo(1));
Assert.That(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"), Is.True);

// The default font sources are missing the two fonts that we are using in this document.
Assert.That(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"), Is.False);
Assert.That(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"), Is.False);

// Use the "SetFontsFolder" method to set a directory which will act as a new font source.
// Pass "false" as the "recursive" argument to include fonts from all the font files that are in the directory
// that we are passing in the first argument, but not include any fonts in any of that directory's subfolders.
// Pass "true" as the "recursive" argument to include all font files in the directory that we are passing
// in the first argument, as well as all the fonts in its subdirectories.
FontSettings.DefaultInstance.SetFontsFolder(FontsDir, recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.That(newFontSources.Length, Is.EqualTo(1));
Assert.That(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"), Is.False);
Assert.That(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"), Is.True);

// The "Amethysta" font is in a subfolder of the font directory.
if (recursive)
{
    Assert.That(newFontSources[0].GetAvailableFonts().Count, Is.EqualTo(30));
    Assert.That(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"), Is.True);
}
else
{
    Assert.That(newFontSources[0].GetAvailableFonts().Count, Is.EqualTo(18));
    Assert.That(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"), Is.False);
}

doc.Save(ArtifactsDir + "FontSettings.SetFontsFolder.pdf");

// Restore the original font sources.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### See Also

* class [FontSettings](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
