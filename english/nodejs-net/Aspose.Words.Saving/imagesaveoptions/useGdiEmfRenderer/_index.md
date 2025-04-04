---
title: ImageSaveOptions.useGdiEmfRenderer property
linktitle: useGdiEmfRenderer property
articleTitle: useGdiEmfRenderer property
second_title: Aspose.Words for Node.js
description: "ImageSaveOptions.useGdiEmfRenderer property. Gets or sets a value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF."
type: docs
weight: 160
url: /nodejs-net/aspose.words.saving/imagesaveoptions/useGdiEmfRenderer/
---

## ImageSaveOptions.useGdiEmfRenderer property

Gets or sets a value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF.


```js
get useGdiEmfRenderer(): boolean
```

### Remarks

If set to ``true`` GDI+ metafile renderer is used. I.e. content is written to GDI+ graphics
object and saved to metafile.

If set to ``false`` Aspose.Words metafile renderer is used. I.e. content is written directly
to the metafile format with Aspose.Words.

Has effect only when saving to EMF.

GDI+ saving works only on .NET.

The default value is ``true``.




### Examples

Shows how to choose a renderer when converting a document to .emf.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.paragraphFormat.style = doc.styles.at("Heading 1");
builder.writeln("Hello world!");
builder.insertImage(base.imageDir + "Logo.jpg");

// When we save the document as an EMF image, we can pass a SaveOptions object to select a renderer for the image.
// If we set the "UseGdiEmfRenderer" flag to "true", Aspose.words will use the GDI+ renderer.
// If we set the "UseGdiEmfRenderer" flag to "false", Aspose.words will use its own metafile renderer.
let saveOptions = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Emf);
saveOptions.useGdiEmfRenderer = useGdiEmfRenderer;

doc.save(base.artifactsDir + "ImageSaveOptions.Renderer.emf", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [ImageSaveOptions](../)

