---
title: MetafileRenderingOptions.emf_plus_dual_rendering_mode property
linktitle: emf_plus_dual_rendering_mode property
articleTitle: emf_plus_dual_rendering_mode property
second_title: Aspose.Words for Python
description: "MetafileRenderingOptions.emf_plus_dual_rendering_mode property. Gets or sets a value determining how EMF+ Dual metafiles should be rendered."
type: docs
weight: 20
url: /python-net/aspose.words.saving/metafilerenderingoptions/emf_plus_dual_rendering_mode/
---

## MetafileRenderingOptions.emf_plus_dual_rendering_mode property

Gets or sets a value determining how EMF+ Dual metafiles should be rendered.


```python
@property
def emf_plus_dual_rendering_mode(self) -> aspose.words.saving.EmfPlusDualRenderingMode:
    ...

@emf_plus_dual_rendering_mode.setter
def emf_plus_dual_rendering_mode(self, value: aspose.words.saving.EmfPlusDualRenderingMode):
    ...

```

### Remarks

EMF+ Dual metafiles contains both EMF+ and EMF parts. MS Word and GDI+ always renders EMF+ part.
Aspose.Words currently doesn't fully supports all EMF+ records and in some cases rendering result of
EMF part looks better then rendering result of EMF+ part.

This option is used only when metafile is rendered as vector graphics. When metafile is rendered
to bitmap, EMF+ part is always used.

The default value is [EmfPlusDualRenderingMode.EMF_PLUS_WITH_FALLBACK](../../emfplusdualrenderingmode/#EMF_PLUS_WITH_FALLBACK).




### Examples

Shows how to configure Enhanced Windows Metafile-related rendering options when saving to PDF.

```python
doc = aw.Document(MY_DIR + "EMF.docx")

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
save_options = aw.saving.PdfSaveOptions()

# Set the "emf_plus_dual_rendering_mode" property to "EmfPlusDualRenderingMode.EMF"
# to only render the EMF part of an EMF+ dual metafile.
# Set the "emf_plus_dual_rendering_mode" property to "EmfPlusDualRenderingMode.EMF_PLUS" to
# to render the EMF+ part of an EMF+ dual metafile.
# Set the "emf_plus_dual_rendering_mode" property to "EmfPlusDualRenderingMode.EMF_PLUS_WITH_FALLBACK"
# to render the EMF+ part of an EMF+ dual metafile if all of the EMF+ records are supported.
# Otherwise, Aspose.Words will render the EMF part.
save_options.metafile_rendering_options.emf_plus_dual_rendering_mode = rendering_mode

# Set the "use_emf_embedded_to_wmf" property to "True" to render embedded EMF data
# for metafiles that we can render as vector graphics.
save_options.metafile_rendering_options.use_emf_embedded_to_wmf = True

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.render_metafile.pdf", save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [MetafileRenderingOptions](../)

