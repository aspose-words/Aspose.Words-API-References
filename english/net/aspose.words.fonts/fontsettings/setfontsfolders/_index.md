---
title: FontSettings.SetFontsFolders
second_title: Aspose.Words for .NET API Reference
description: FontSettings method. Sets the folders where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts in C#.
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

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// The default font sources are missing the two fonts that we are using in this document.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Use the "SetFontsFolders" method to create a font source from each font directory that we pass as the first argument.
// Pass "false" as the "recursive" argument to include fonts from all the font files that are in the directories
// that we are passing in the first argument, but not include any fonts from any of the directories' subfolders.
// Pass "true" as the "recursive" argument to include all font files in the directories that we are passing
// in the first argument, as well as all the fonts in their subdirectories.
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// The "Junction" folder itself contains no font files, but has subfolders that do.
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

// Restore the original font sources.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### See Also

* class [FontSettings](../)
* namespace [Aspose.Words.Fonts](../../fontsettings/)
* assembly [Aspose.Words](../../../)
