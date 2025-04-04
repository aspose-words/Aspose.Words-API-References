---
title: MetafileRenderingOptions.emulateRenderingToSizeOnPageResolution property
linktitle: emulateRenderingToSizeOnPageResolution property
articleTitle: emulateRenderingToSizeOnPageResolution property
second_title: Aspose.Words for Node.js
description: "MetafileRenderingOptions.emulateRenderingToSizeOnPageResolution property. Gets or sets the resolution in pixels per inch for the emulation of metafile rendering to the size on page."
type: docs
weight: 50
url: /nodejs-net/aspose.words.saving/metafilerenderingoptions/emulateRenderingToSizeOnPageResolution/
---

## MetafileRenderingOptions.emulateRenderingToSizeOnPageResolution property

Gets or sets the resolution in pixels per inch for the emulation of metafile rendering to the size on page.


```js
get emulateRenderingToSizeOnPageResolution(): number
```

### Remarks

This option is used only when [MetafileRenderingOptions.emulateRenderingToSizeOnPage](../emulateRenderingToSizeOnPage/) is set to ``true``.

The default value is 96. This is a default display resolution. I.e. metafile rendering will emulate the display of
the metafile in MS Word with a 100% zoom factor.




### Examples

Shows how to display of the metafile according to the size on page.

```js
let doc = new aw.Document(base.myDir + "WMF with text.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let saveOptions = new aw.Saving.PdfSaveOptions();


// Set the "EmulateRenderingToSizeOnPage" property to "true"
// to emulate rendering according to the metafile size on page.
// Set the "EmulateRenderingToSizeOnPage" property to "false"
// to emulate metafile rendering to its default size in pixels.
saveOptions.metafileRenderingOptions.emulateRenderingToSizeOnPage = renderToSize;
saveOptions.metafileRenderingOptions.emulateRenderingToSizeOnPageResolution = 50;

doc.save(base.artifactsDir + "PdfSaveOptions.emulateRenderingToSizeOnPage.pdf", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [MetafileRenderingOptions](../)

