---
title: ImageSaveOptions.use_gdi_emf_renderer property
linktitle: use_gdi_emf_renderer property
articleTitle: use_gdi_emf_renderer property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.use_gdi_emf_renderer property. Gets or sets a value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF."
type: docs
weight: 170
url: /python-net/aspose.words.saving/imagesaveoptions/use_gdi_emf_renderer/
---

## ImageSaveOptions.use_gdi_emf_renderer property

Gets or sets a value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF.


```python
@property
def use_gdi_emf_renderer(self) -> bool:
    ...

@use_gdi_emf_renderer.setter
def use_gdi_emf_renderer(self, value: bool):
    ...

```

### Remarks

If set to ``True`` GDI+ metafile renderer is used. I.e. content is written to GDI+ graphics
object and saved to metafile.

If set to ``False`` Aspose.Words metafile renderer is used. I.e. content is written directly
to the metafile format with Aspose.Words.

Has effect only when saving to EMF.

GDI+ saving works only on .NET.

The default value is ``True``.




### Examples

Shows how to choose a renderer when converting a document to .emf.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('Hello world!')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# When we save the document as an EMF image, we can pass a SaveOptions object to select a renderer for the image.
# If we set the "UseGdiEmfRenderer" flag to "true", Aspose.Words will use the GDI+ renderer.
# If we set the "UseGdiEmfRenderer" flag to "false", Aspose.Words will use its own metafile renderer.
save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.EMF)
save_options.use_gdi_emf_renderer = use_gdi_emf_renderer
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.Renderer.emf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

