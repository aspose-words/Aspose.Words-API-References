---
title: MetafileRenderingOptions.use_emf_embedded_to_wmf property
linktitle: use_emf_embedded_to_wmf property
articleTitle: use_emf_embedded_to_wmf property
second_title: Aspose.Words for Python
description: "MetafileRenderingOptions.use_emf_embedded_to_wmf property. Gets or sets a value determining how WMF metafiles with embedded EMF metafiles should be rendered."
type: docs
weight: 70
url: /python-net/aspose.words.saving/metafilerenderingoptions/use_emf_embedded_to_wmf/
---

## MetafileRenderingOptions.use_emf_embedded_to_wmf property

Gets or sets a value determining how WMF metafiles with embedded EMF metafiles should be rendered.


```python
@property
def use_emf_embedded_to_wmf(self) -> bool:
    ...

@use_emf_embedded_to_wmf.setter
def use_emf_embedded_to_wmf(self, value: bool):
    ...

```

### Remarks

WMF metafiles could contain embedded EMF data. MS Word in most cases uses embedded EMF data.
GDI+ always uses WMF data.

When this value is set to ``True``, Aspose.Words uses embedded EMF data when rendering.

When this value is set to ``False``, Aspose.Words uses WMF data when rendering.

This option is used only when metafile is rendered as vector graphics. When metafile is rendered
to bitmap, WMF data is always used.

The default value is ``True``.




### Examples

Shows how to configure Enhanced Windows Metafile-related rendering options when saving to PDF.

```python
doc = aw.Document(file_name=MY_DIR + 'EMF.docx')
# Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
# to modify how that method converts the document to .PDF.
save_options = aw.saving.PdfSaveOptions()
# Set the "EmfPlusDualRenderingMode" property to "EmfPlusDualRenderingMode.Emf"
# to only render the EMF part of an EMF+ dual metafile.
# Set the "EmfPlusDualRenderingMode" property to "EmfPlusDualRenderingMode.EmfPlus" to
# to render the EMF+ part of an EMF+ dual metafile.
# Set the "EmfPlusDualRenderingMode" property to "EmfPlusDualRenderingMode.EmfPlusWithFallback"
# to render the EMF+ part of an EMF+ dual metafile if all of the EMF+ records are supported.
# Otherwise, Aspose.Words will render the EMF part.
save_options.metafile_rendering_options.emf_plus_dual_rendering_mode = rendering_mode
# Set the "UseEmfEmbeddedToWmf" property to "true" to render embedded EMF data
# for metafiles that we can render as vector graphics.
save_options.metafile_rendering_options.use_emf_embedded_to_wmf = True
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.RenderMetafile.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [MetafileRenderingOptions](../)

