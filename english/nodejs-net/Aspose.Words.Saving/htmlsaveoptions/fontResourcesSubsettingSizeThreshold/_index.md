---
title: HtmlSaveOptions.fontResourcesSubsettingSizeThreshold property
linktitle: fontResourcesSubsettingSizeThreshold property
articleTitle: fontResourcesSubsettingSizeThreshold property
second_title: Aspose.Words for NodeJs
description: "HtmlSaveOptions.fontResourcesSubsettingSizeThreshold property. Controls which font resources need subsetting when saving to HTML, MHTML or EPUB"
type: docs
weight: 290
url: /nodejs-net/Aspose.Words.Saving/htmlsaveoptions/fontResourcesSubsettingSizeThreshold/
---

## HtmlSaveOptions.fontResourcesSubsettingSizeThreshold property

Controls which font resources need subsetting when saving to HTML, MHTML or EPUB.
Default is ``0``.



```js
get fontResourcesSubsettingSizeThreshold(): number
```

### Remarks

[HtmlSaveOptions.exportFontResources](../exportFontResources/) allows exporting fonts as subsidiary files or as parts of the output
package. If the document uses many fonts, especially with large number of glyphs, then output size can grow
significantly. Font subsetting reduces the size of the exported font resource by filtering out glyphs that
are not used by the current document.

Font subsetting works as follows:


* By default, all exported fonts are subsetted.
  
* Setting [HtmlSaveOptions.fontResourcesSubsettingSizeThreshold](./) to a positive value 
  instructs Aspose.Words to subset fonts which file size is larger than the specified value.
  
* Setting the property to int.MaxValue C# constant
  suppresses font subsetting.
  
**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable
font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not
allow web downloading of their fonts in any form. License agreements that cover some fonts specifically note that usage via **@font-face** rules
in CSS style sheets is not allowed. Font subsetting can also violate license terms.





### Examples

Shows how to work with font subsetting.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.font.name = "Arial";
builder.writeln("Hello world!");
builder.font.name = "Times New Roman";
builder.writeln("Hello world!");
builder.font.name = "Courier New";
builder.writeln("Hello world!");

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
let fontsFolder = base.artifactsDir + "HtmlSaveOptions.FontSubsetting.Fonts";

let options = new aw.Saving.HtmlSaveOptions();
options.exportFontResources = true;
options.fontsFolder = fontsFolder;
options.fontResourcesSubsettingSizeThreshold = fontResourcesSubsettingSizeThreshold;

doc.save(base.artifactsDir + "HtmlSaveOptions.FontSubsetting.html", options);

let fontFileNames = fs.readdirSync(fontsFolder).filter(s => s.endsWith(".ttf"));

expect(fontFileNames.length).toEqual(3);

for (let filename of fontFileNames)
{
  // By default, the .ttf files for each of our three fonts will be over 700MB.
  // Subsetting will reduce them all to under 30MB.
  let fontFileInfo = fs.statSync(path.join(fontsFolder, filename));

  expect(fontFileInfo.size > 700000 || fontFileInfo.size < 30000).toEqual(true);
  expect(Math.max(fontResourcesSubsettingSizeThreshold, 30000) > fontFileInfo.size).toEqual(true);
}
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.exportFontResources](../exportFontResources/)

