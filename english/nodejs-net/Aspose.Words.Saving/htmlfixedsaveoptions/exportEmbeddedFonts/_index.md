---
title: HtmlFixedSaveOptions.exportEmbeddedFonts property
linktitle: exportEmbeddedFonts property
articleTitle: exportEmbeddedFonts property
second_title: Aspose.Words for NodeJs
description: "HtmlFixedSaveOptions.exportEmbeddedFonts property. Specifies whether fonts should be embedded into Html document in Base64 format"
type: docs
weight: 50
url: /nodejs-net/aspose.words.saving/htmlfixedsaveoptions/exportEmbeddedFonts/
---

## HtmlFixedSaveOptions.exportEmbeddedFonts property

Specifies whether fonts should be embedded into Html document in Base64 format.
Note setting this flag can significantly increase size of output Html file.


```js
get exportEmbeddedFonts(): boolean
```

### Examples

Shows how to determine where to store embedded fonts when exporting a document to Html.

```js
let doc = new aw.Document(base.myDir + "Embedded font.docx");

// When we export a document with embedded fonts to .html,
// Aspose.words can place the fonts in two possible locations.
// Setting the "ExportEmbeddedFonts" flag to "true" will store the raw data for embedded fonts within the CSS stylesheet,
// in the "url" property of the "@font-face" rule. This may create a huge CSS stylesheet file
// and reduce the number of external files that this HTML conversion will create.
// Setting this flag to "false" will create a file for each font.
// The CSS stylesheet will link to each font file using the "url" property of the "@font-face" rule.
let htmlFixedSaveOptions = new aw.Saving.HtmlFixedSaveOptions();
htmlFixedSaveOptions.exportEmbeddedFonts = exportEmbeddedFonts;

const outPath = path.join(base.artifactsDir, "HtmlFixedSaveOptions.exportEmbeddedFonts");
if (fs.existsSync(outPath))
  fs.rmSync(outPath, {recursive: true, force: true} );

doc.save(outPath + ".html", htmlFixedSaveOptions);
let outDocContents = fs.readFileSync(path.join(outPath, "styles.css")).toString();

if (exportEmbeddedFonts)
{
  const patternEmbedded = /@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local\('☺'\), url\(.+\) format\('woff'\); }/;
  expect(patternEmbedded.test(outDocContents)).toBeTruthy();
  expect(fs.readdirSync(outPath).filter(f => f.endsWith(".woff")).length).toEqual(0);
}
else
{
  expect(outDocContents.includes("@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local('☺'), url('font001.woff') format('woff'); }")).toBeTruthy();
  expect(fs.readdirSync(outPath).filter(f => f.endsWith(".woff")).length).toEqual(2);
}
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlFixedSaveOptions](../)

