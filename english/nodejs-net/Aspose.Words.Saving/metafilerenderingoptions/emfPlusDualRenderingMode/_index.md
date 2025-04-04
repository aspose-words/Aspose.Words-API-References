---
title: MetafileRenderingOptions.emfPlusDualRenderingMode property
linktitle: emfPlusDualRenderingMode property
articleTitle: emfPlusDualRenderingMode property
second_title: Aspose.Words for Node.js
description: "MetafileRenderingOptions.emfPlusDualRenderingMode property. Gets or sets a value determining how EMF+ Dual metafiles should be rendered."
type: docs
weight: 20
url: /nodejs-net/aspose.words.saving/metafilerenderingoptions/emfPlusDualRenderingMode/
---

## MetafileRenderingOptions.emfPlusDualRenderingMode property

Gets or sets a value determining how EMF+ Dual metafiles should be rendered.


```js
get emfPlusDualRenderingMode(): Aspose.Words.Saving.EmfPlusDualRenderingMode
```

### Remarks

EMF+ Dual metafiles contains both EMF+ and EMF parts. MS Word and GDI+ always renders EMF+ part.
Aspose.Words currently doesn't fully supports all EMF+ records and in some cases rendering result of
EMF part looks better then rendering result of EMF+ part.

This option is used only when metafile is rendered as vector graphics. When metafile is rendered
to bitmap, EMF+ part is always used.

The default value is [EmfPlusDualRenderingMode.EmfPlusWithFallback](../../emfplusdualrenderingmode/#EmfPlusWithFallback).




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

