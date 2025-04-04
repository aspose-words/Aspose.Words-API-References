---
title: HtmlFixedSaveOptions.exportEmbeddedImages property
linktitle: exportEmbeddedImages property
articleTitle: exportEmbeddedImages property
second_title: Aspose.Words for Node.js
description: "HtmlFixedSaveOptions.exportEmbeddedImages property. Specifies whether images should be embedded into Html document in Base64 format"
type: docs
weight: 60
url: /nodejs-net/aspose.words.saving/htmlfixedsaveoptions/exportEmbeddedImages/
---

## HtmlFixedSaveOptions.exportEmbeddedImages property

Specifies whether images should be embedded into Html document in Base64 format.
Note setting this flag can significantly increase size of output Html file.


```js
get exportEmbeddedImages(): boolean
```

### Examples

Shows how to determine where to store images when exporting a document to Html.

```js
let doc = new aw.Document(base.myDir + "Images.docx");

// When we export a document with embedded images to .html,
// Aspose.words can place the images in two possible locations.
// Setting the "ExportEmbeddedImages" flag to "true" will store the raw data
// for all images within the output HTML document, in the "src" attribute of <image> tags.
// Setting this flag to "false" will create an image file in the local file system for every image,
// and store all these files in a separate folder.
let htmlFixedSaveOptions = new aw.Saving.HtmlFixedSaveOptions();
htmlFixedSaveOptions.exportEmbeddedImages = exportImages;

const outPath = path.join(base.artifactsDir, "HtmlFixedSaveOptions.exportEmbeddedImages");
if (fs.existsSync(outPath))
  fs.rmSync(outPath, {recursive: true, force: true} );

doc.save(outPath + ".html", htmlFixedSaveOptions);
let outDocContents = fs.readFileSync(outPath + ".html").toString();

if (exportImages)
{
  expect(fs.existsSync(path.join(outPath, "image001.jpeg"))).toBeFalsy();
  expect(new RegExp("<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" src=\".+\" />").test(outDocContents)).toBeTruthy();
}
else
{
  expect(fs.existsSync(path.join(outPath, "image001.jpeg"))).toBeTruthy();
  expect(outDocContents.includes("<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" " +
    "src=\"HtmlFixedSaveOptions.exportEmbeddedImages/image001.jpeg\" />")).toBeTruthy();
}
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlFixedSaveOptions](../)

