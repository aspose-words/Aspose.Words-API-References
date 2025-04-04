---
title: HtmlSaveOptions.exportImagesAsBase64 property
linktitle: exportImagesAsBase64 property
articleTitle: exportImagesAsBase64 property
second_title: Aspose.Words for Node.js
description: "HtmlSaveOptions.exportImagesAsBase64 property. Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB"
type: docs
weight: 170
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/exportImagesAsBase64/
---

## HtmlSaveOptions.exportImagesAsBase64 property

Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB.
Default is ``false``.



```js
get exportImagesAsBase64(): boolean
```

### Remarks

When this property is set to ``true`` images data are exported
directly into the **img** elements and separate files are not created.




### Examples

Shows how to save a .html document with images embedded inside it.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

let options = new aw.Saving.HtmlSaveOptions();
options.exportImagesAsBase64 = exportImagesAsBase64;
options.prettyFormat = true;

doc.save(base.artifactsDir + "HtmlSaveOptions.exportImagesAsBase64.html", options);

let outDocContents = fs.readFileSync(base.artifactsDir + "HtmlSaveOptions.exportImagesAsBase64.html").toString();

expect(exportImagesAsBase64
  ? outDocContents.includes("<img src=\"data:image/png;base64")
  : outDocContents.includes("<img src=\"HtmlSaveOptions.exportImagesAsBase64.001.png\"")).toBe(true);
```

Shows how to embed fonts inside a saved HTML document.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

let options = new aw.Saving.HtmlSaveOptions();
options.exportFontsAsBase64 = true;
options.cssStyleSheetType = aw.Saving.CssStyleSheetType.Embedded;
options.prettyFormat = true;

doc.save(base.artifactsDir + "HtmlSaveOptions.exportFontsAsBase64.html", options);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)

