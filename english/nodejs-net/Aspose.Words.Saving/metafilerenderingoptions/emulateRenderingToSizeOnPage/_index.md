---
title: MetafileRenderingOptions.emulateRenderingToSizeOnPage property
linktitle: emulateRenderingToSizeOnPage property
articleTitle: emulateRenderingToSizeOnPage property
second_title: Aspose.Words for NodeJs
description: "MetafileRenderingOptions.emulateRenderingToSizeOnPage property. Gets or sets a value determining whether metafile rendering emulates the display of the metafile according to the size on page or the display of the metafile in its default size."
type: docs
weight: 40
url: /nodejs-net/aspose.words.saving/metafilerenderingoptions/emulateRenderingToSizeOnPage/
---

## MetafileRenderingOptions.emulateRenderingToSizeOnPage property

Gets or sets a value determining whether metafile rendering emulates the display of the metafile according to the size on page
or the display of the metafile in its default size.


```js
get emulateRenderingToSizeOnPage(): boolean
```

### Remarks

When metafiles are displayed in MS Word, some graphics may be scaled according to the actual metafile size in pixels.
I.e. even zooming may affect the metafile display.

When this value is set to ``true``, Aspose.Words emulates rendering according to the metafile size on page.
The size in pixels is calculated from the metafile size on the page and the specified [MetafileRenderingOptions.emulateRenderingToSizeOnPageResolution](../emulateRenderingToSizeOnPageResolution/).

When this value is set to ``false``, Aspose.Words emulates metafile rendering to its default size in pixels.

This option is used only when metafile is rendered as vector graphics.

The default value is ``true``.




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

