---
title: HtmlSaveOptions.metafileFormat property
linktitle: metafileFormat property
articleTitle: metafileFormat property
second_title: Aspose.Words for Node.js
description: "HtmlSaveOptions.metafileFormat property. Specifies in what format metafiles are saved when exporting to HTML, MHTML, or EPUB"
type: docs
weight: 380
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/metafileFormat/
---

## HtmlSaveOptions.metafileFormat property

Specifies in what format metafiles are saved when exporting to HTML, MHTML, or EPUB.
Default value is [HtmlMetafileFormat.Png](../../htmlmetafileformat/#Png), meaning that metafiles are rendered to raster PNG images.



```js
get metafileFormat(): Aspose.Words.Saving.HtmlMetafileFormat
```

### Remarks

Metafiles are not natively displayed by HTML browsers. By default, Aspose.Words converts WMF and EMF 
images into PNG files when exporting to HTML. Other options are to convert metafiles to SVG images or to export
them as is without conversion.

Some image transforms, in particular image cropping, will not be applied to metafile images if they
are exported to HTML without conversion.




### Examples

Shows how to convert SVG objects to a different format when saving HTML documents.

```js
let html = 
  `<html>
    <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>
      <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>
    </svg>
  </html>`

// Use 'ConvertSvgToEmf' to turn back the legacy behavior
// where all SVG images loaded from an HTML document were converted to EMF.
// Now SVG images are loaded without conversion
// if the MS Word version specified in load options supports SVG images natively.
let loadOptions = new aw.Loading.HtmlLoadOptions();
loadOptions.convertSvgToEmf = true;

let doc = new aw.Document(Buffer.from(html, 'utf-8'), loadOptions);

// This document contains a <svg> element in the form of text.
// When we save the document to HTML, we can pass a SaveOptions object
// to determine how the saving operation handles this object.
// Setting the "MetafileFormat" property to "HtmlMetafileFormat.Png" to convert it to a PNG image.
// Setting the "MetafileFormat" property to "HtmlMetafileFormat.Svg" preserve it as a SVG object.
// Setting the "MetafileFormat" property to "HtmlMetafileFormat.EmfOrWmf" to convert it to a metafile.
let options = new aw.Saving.HtmlSaveOptions();
options.metafileFormat = htmlMetafileFormat;

doc.save(base.artifactsDir + "HtmlSaveOptions.metafileFormat.html", options);

let outDocContents = fs.readFileSync(base.artifactsDir + "HtmlSaveOptions.metafileFormat.html").toString();

switch (htmlMetafileFormat)
{
  case aw.Saving.HtmlMetafileFormat.Png:
    expect(outDocContents.includes(
                    "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                        "<img src=\"HtmlSaveOptions.metafileFormat.001.png\" width=\"500\" height=\"40\" alt=\"\" " +
                        "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
                    "</p>")).toEqual(true);
    break;
  case aw.Saving.HtmlMetafileFormat.Svg:
    expect(outDocContents.includes(
                    "<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">" +
                    "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"499\" height=\"40\">")).toEqual(true);
    break;
  case aw.Saving.HtmlMetafileFormat.EmfOrWmf:
    expect(outDocContents.includes(
                    "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                        "<img src=\"HtmlSaveOptions.metafileFormat.001.emf\" width=\"500\" height=\"40\" alt=\"\" " +
                        "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
                    "</p>")).toEqual(true);
    break;
}
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.imageResolution](../imageResolution/)
* property [HtmlSaveOptions.scaleImageToShapeSize](../scaleImageToShapeSize/)

