---
title: FontSettings.SetFontsFolders
linktitle: SetFontsFolders
articleTitle: SetFontsFolders
second_title: Aspose.Words for .NET
description: Discover how to use the SetFontsFolders method in Aspose.Words to customize TrueType font locations for optimal document rendering and embedding.
type: docs
weight: 90
url: /net/aspose.words.fonts/fontsettings/setfontsfolders/
---
## FontSettings.SetFontsFolders method

Sets the folders where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts.

```csharp
public void SetFontsFolders(string[] fontsFolders, bool recursive)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fontsFolders | String[] | An array of folders that contain TrueType fonts. |
| recursive | Boolean | True to scan the specified folders for fonts recursively. |

## Remarks

By default, Aspose.Words looks for fonts installed to the system.

Setting this property resets the cache of all previously loaded fonts.

## Examples

Shows how to set multiple font source directories.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Our font sources do not contain the font that we have used for text in this document.
// If we use these font settings while rendering this document,
// Aspose.Words will apply a fallback font to text which has a font that Aspose.Words cannot locate.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.That(originalFontSources.Length, Is.EqualTo(1));
Assert.That(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"), Is.True);

// The default font sources are missing the two fonts that we are using in this document.
Assert.That(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"), Is.False);
Assert.That(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"), Is.False);

// Use the "SetFontsFolders" method to create a font source from each font directory that we pass as the first argument.
// Pass "false" as the "recursive" argument to include fonts from all the font files that are in the directories
// that we are passing in the first argument, but not include any fonts from any of the directories' subfolders.
// Pass "true" as the "recursive" argument to include all font files in the directories that we are passing
// in the first argument, as well as all the fonts in their subdirectories.
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.That(newFontSources.Length, Is.EqualTo(2));
Assert.That(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"), Is.False);
Assert.That(newFontSources[0].GetAvailableFonts().Count, Is.EqualTo(1));
Assert.That(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"), Is.True);

// The "Junction" folder itself contains no font files, but has subfolders that do.
if (recursive)
{
    Assert.That(newFontSources[1].GetAvailableFonts().Count, Is.EqualTo(11));
    Assert.That(newFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"), Is.True);
}
else
{
    Assert.That(newFontSources[1].GetAvailableFonts().Count, Is.EqualTo(0));
}

doc.Save(ArtifactsDir + "FontSettings.SetFontsFolders.pdf");

// Restore the original font sources.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### See Also

* class [FontSettings](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
