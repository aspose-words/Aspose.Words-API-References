---
title: MetafileRenderingOptions.useEmfEmbeddedToWmf property
linktitle: useEmfEmbeddedToWmf property
articleTitle: useEmfEmbeddedToWmf property
second_title: Aspose.Words for NodeJs
description: "MetafileRenderingOptions.useEmfEmbeddedToWmf property. Gets or sets a value determining how WMF metafiles with embedded EMF metafiles should be rendered."
type: docs
weight: 70
url: /nodejs-net/Aspose.Words.Saving/metafilerenderingoptions/useEmfEmbeddedToWmf/
---

## MetafileRenderingOptions.useEmfEmbeddedToWmf property

Gets or sets a value determining how WMF metafiles with embedded EMF metafiles should be rendered.


```js
get useEmfEmbeddedToWmf(): boolean
```

### Remarks

WMF metafiles could contain embedded EMF data. MS Word in most cases uses embedded EMF data.
GDI+ always uses WMF data.

When this value is set to ``true``, Aspose.Words uses embedded EMF data when rendering.

When this value is set to ``false``, Aspose.Words uses WMF data when rendering.

This option is used only when metafile is rendered as vector graphics. When metafile is rendered
to bitmap, WMF data is always used.

The default value is ``true``.




### Examples

Shows how to configure Enhanced Windows Metafile-related rendering options when saving to PDF.

```js
let doc = new aw.Document(base.myDir + "EMF.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let saveOptions = new aw.Saving.PdfSaveOptions();

// Set the "EmfPlusDualRenderingMode" property to "EmfPlusDualRenderingMode.Emf"
// to only render the EMF part of an EMF+ dual metafile.
// Set the "EmfPlusDualRenderingMode" property to "EmfPlusDualRenderingMode.EmfPlus" to
// to render the EMF+ part of an EMF+ dual metafile.
// Set the "EmfPlusDualRenderingMode" property to "EmfPlusDualRenderingMode.EmfPlusWithFallback"
// to render the EMF+ part of an EMF+ dual metafile if all of the EMF+ records are supported.
// Otherwise, Aspose.words will render the EMF part.
saveOptions.metafileRenderingOptions.emfPlusDualRenderingMode = renderingMode;

// Set the "UseEmfEmbeddedToWmf" property to "true" to render embedded EMF data
// for metafiles that we can render as vector graphics.
saveOptions.metafileRenderingOptions.useEmfEmbeddedToWmf = true;

doc.save(base.artifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [MetafileRenderingOptions](../)

