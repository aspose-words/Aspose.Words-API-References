---
title: HtmlFixedSaveOptions.exportEmbeddedSvg property
linktitle: exportEmbeddedSvg property
articleTitle: exportEmbeddedSvg property
second_title: Aspose.Words for NodeJs
description: "HtmlFixedSaveOptions.exportEmbeddedSvg property. Specifies whether SVG resources should be embedded into Html document"
type: docs
weight: 70
url: /nodejs-net/Aspose.Words.Saving/htmlfixedsaveoptions/exportEmbeddedSvg/
---

## HtmlFixedSaveOptions.exportEmbeddedSvg property

Specifies whether SVG resources should be embedded into Html document.
Default value is ``True``.



```js
get exportEmbeddedSvg(): boolean
```

### Examples

Shows how to determine where to store SVG objects when exporting a document to Html.

```js
let doc = new aw.Document(base.myDir + "Images.docx");

// When we export a document with SVG objects to .html,
// Aspose.words can place these objects in two possible locations.
// Setting the "ExportEmbeddedSvg" flag to "true" will embed all SVG object raw data
// within the output HTML, inside <image> tags.
// Setting this flag to "false" will create a file in the local file system for each SVG object.
// The HTML will link to each file using the "data" attribute of an <object> tag.
let htmlFixedSaveOptions = new aw.Saving.HtmlFixedSaveOptions();
htmlFixedSaveOptions.exportEmbeddedSvg = exportSvgs;

const outPath = path.join(base.artifactsDir, "HtmlFixedSaveOptions.ExportEmbeddedSvgs");
if (fs.existsSync(outPath))
  fs.rmSync(outPath, {recursive: true, force: true} );

doc.save(outPath + ".html", htmlFixedSaveOptions);
let outDocContents = fs.readFileSync(outPath + ".html").toString();

if (exportSvgs)
{
  expect(fs.existsSync(path.join(outPath, "svg001.svg"))).toBeFalsy();
  const pattern = /<image id="image004" xlink:href=.+\/>/;      
  expect(pattern.test(outDocContents)).toBeTruthy();
}
else
{
  expect(fs.existsSync(path.join(outPath, "svg001.svg"))).toBeTruthy();
  const pattern = /<object type="image\/svg\+xml" data="HtmlFixedSaveOptions.ExportEmbeddedSvgs\/svg001\.svg"><\/object>/;
  expect(pattern.test(outDocContents)).toBeTruthy();
}
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlFixedSaveOptions](../)

