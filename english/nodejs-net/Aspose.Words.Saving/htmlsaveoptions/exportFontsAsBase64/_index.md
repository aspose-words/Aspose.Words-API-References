---
title: HtmlSaveOptions.exportFontsAsBase64 property
linktitle: exportFontsAsBase64 property
articleTitle: exportFontsAsBase64 property
second_title: Aspose.Words for NodeJs
description: "HtmlSaveOptions.exportFontsAsBase64 property. Specifies whether fonts resources should be embedded to HTML in Base64 encoding"
type: docs
weight: 150
url: /nodejs-net/Aspose.Words.Saving/htmlsaveoptions/exportFontsAsBase64/
---

## HtmlSaveOptions.exportFontsAsBase64 property

Specifies whether fonts resources should be embedded to HTML in Base64 encoding.
Default is ``false``.



```js
get exportFontsAsBase64(): boolean
```

### Remarks

By default, fonts are written to separate files. If this option is set to ``true``, fonts will be embedded
into the document's CSS in Base64 encoding.




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

