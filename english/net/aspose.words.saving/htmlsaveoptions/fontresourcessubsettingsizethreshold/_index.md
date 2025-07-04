---
title: HtmlSaveOptions.FontResourcesSubsettingSizeThreshold
linktitle: FontResourcesSubsettingSizeThreshold
articleTitle: FontResourcesSubsettingSizeThreshold
second_title: Aspose.Words for .NET
description: Optimize your HTML, MHTML, or EPUB files with the FontResourcesSubsettingSizeThreshold property, ensuring efficient font resource management. Default, 0.
type: docs
weight: 290
url: /net/aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions.FontResourcesSubsettingSizeThreshold property

Controls which font resources need subsetting when saving to HTML, MHTML or EPUB. Default is `0`.

```csharp
public int FontResourcesSubsettingSizeThreshold { get; set; }
```

## Remarks

[`ExportFontResources`](../exportfontresources/) allows exporting fonts as subsidiary files or as parts of the output package. If the document uses many fonts, especially with large number of glyphs, then output size can grow significantly. Font subsetting reduces the size of the exported font resource by filtering out glyphs that are not used by the current document.

Font subsetting works as follows:

* By default, all exported fonts are subsetted.
* Setting `FontResourcesSubsettingSizeThreshold` to a positive value instructs Aspose.Words to subset fonts which file size is larger than the specified value.
* Setting the property to MaxValue suppresses font subsetting.

**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. License agreements that cover some fonts specifically note that usage via **@font-face** rules in CSS style sheets is not allowed. Font subsetting can also violate license terms.

## Examples

Shows how to work with font subsetting.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Times New Roman";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("Hello world!");

// When we save the document to HTML, we can pass a SaveOptions object configure font subsetting.
// Suppose we set the "ExportFontResources" flag to "true" and also name a folder in the "FontsFolder" property.
// In that case, the saving operation will create that folder and place a .ttf file inside
// that folder for each font that our document uses.
// Each .ttf file will contain that font's entire glyph set,
// which may potentially result in a very large file that accompanies the document.
// When we apply subsetting to a font, its exported raw data will only contain the glyphs that the document is
// using instead of the entire glyph set. If the text in our document only uses a small fraction of a font's
// glyph set, then subsetting will significantly reduce our output documents' size.
// We can use the "FontResourcesSubsettingSizeThreshold" property to define a .ttf file size, in bytes.
// If an exported font creates a size bigger file than that, then the save operation will apply subsetting to that font. 
// Setting a threshold of 0 applies subsetting to all fonts,
// and setting it to "int.MaxValue" effectively disables subsetting.
string fontsFolder = ArtifactsDir + "HtmlSaveOptions.FontSubsetting.Fonts";

HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportFontResources = true,
    FontsFolder = fontsFolder,
    FontResourcesSubsettingSizeThreshold = fontResourcesSubsettingSizeThreshold
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FontSubsetting.html", options);

string[] fontFileNames = Directory.GetFiles(fontsFolder).Where(s => s.EndsWith(".ttf")).ToArray();

Assert.That(fontFileNames.Length, Is.EqualTo(3));

foreach (string filename in fontFileNames)
{
    // By default, the .ttf files for each of our three fonts will be over 700MB.
    // Subsetting will reduce them all to under 30MB.
    FileInfo fontFileInfo = new FileInfo(filename);

    Assert.That(fontFileInfo.Length > 700000 || fontFileInfo.Length < 30000, Is.True);
    Assert.That(System.Math.Max(fontResourcesSubsettingSizeThreshold, 30000) > new FileInfo(filename).Length, Is.True);
}
```

### See Also

* class [HtmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
