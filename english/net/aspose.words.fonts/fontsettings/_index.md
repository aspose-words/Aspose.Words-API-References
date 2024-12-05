---
title: FontSettings Class
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words for .NET
description: Aspose.Words.Fonts.FontSettings class. Specifies font settings for a document in C#.
type: docs
weight: 3370
url: /net/aspose.words.fonts/fontsettings/
---
## FontSettings class

Specifies font settings for a document.

To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/net/working-with-fonts/) documentation article.

```csharp
public class FontSettings
```

## Constructors

| Name | Description |
| --- | --- |
| [FontSettings](fontsettings/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| static [DefaultInstance](../../aspose.words.fonts/fontsettings/defaultinstance/) { get; } | Static default font settings. |
| [FallbackSettings](../../aspose.words.fonts/fontsettings/fallbacksettings/) { get; } | Settings related to font fallback mechanism. |
| [SubstitutionSettings](../../aspose.words.fonts/fontsettings/substitutionsettings/) { get; } | Settings related to font substitution mechanism. |

## Methods

| Name | Description |
| --- | --- |
| [GetFontsSources](../../aspose.words.fonts/fontsettings/getfontssources/)() | Gets a copy of the array that contains the list of sources where Aspose.Words looks for TrueType fonts. |
| [ResetFontSources](../../aspose.words.fonts/fontsettings/resetfontsources/)() | Resets the fonts sources to the system default. |
| [SaveSearchCache](../../aspose.words.fonts/fontsettings/savesearchcache/)(*Stream*) | Saves the font search cache to the stream. |
| [SetFontsFolder](../../aspose.words.fonts/fontsettings/setfontsfolder/)(*string, bool*) | Sets the folder where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts. This is a shortcut to [`SetFontsFolders`](./setfontsfolders/) for setting only one font directory. |
| [SetFontsFolders](../../aspose.words.fonts/fontsettings/setfontsfolders/)(*string[], bool*) | Sets the folders where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources)(*FontSourceBase[]*) | Sets the sources where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources_1)(*FontSourceBase[], Stream*) | Sets the sources where Aspose.Words looks for TrueType fonts and additionally loads previously saved font search cache. |

## Remarks

Aspose.Words uses font settings to resolve the fonts in the document. Fonts are resolved mostly when building document layout or rendering to fixed page formats. But when loading some formats, Aspose.Words also may require to resolve the fonts. For example, when loading HTML documents Aspose.Words may resolve the fonts to perform font fallback. So it is recommended that you set the font settings in [`LoadOptions`](../../aspose.words.loading/loadoptions/) when loading the document. Or at least before building the layout or rendering the document to the fixed-page format.

By default all documents uses single static font settings instance. It could be accessed by [`DefaultInstance`](./defaultinstance/) property.

Changing font settings is safe at any time from any thread. But it is recommended that you do not change the font settings while processing some documents which uses this settings. This can lead to the fact that the same font will be resolved differently in different parts of the document.

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

Assert.AreEqual(1, originalFontSources.Length);

Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// The default font source is missing two of the fonts that we are using in our document.
// When we save this document, Aspose.Words will apply fallback fonts to all text formatted with inaccessible fonts.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Create a font source from a folder that contains fonts.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Apply a new array of font sources that contains the original font sources, as well as our custom fonts.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// Verify that Aspose.Words has access to all required fonts before we render the document to PDF.
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.True(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

// Restore the original font sources.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

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

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// The default font sources are missing the two fonts that we are using in this document.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Use the "SetFontsFolder" method to set a directory which will act as a new font source.
// Pass "false" as the "recursive" argument to include fonts from all the font files that are in the directory
// that we are passing in the first argument, but not include any fonts in any of that directory's subfolders.
// Pass "true" as the "recursive" argument to include all font files in the directory that we are passing
// in the first argument, as well as all the fonts in its subdirectories.
FontSettings.DefaultInstance.SetFontsFolder(FontsDir, recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// The "Amethysta" font is in a subfolder of the font directory.
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

// Restore the original font sources.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

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

* namespace [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assembly [Aspose.Words](../../)
