---
title: MetafileRenderingOptions.use_emf_embedded_to_wmf property
linktitle: use_emf_embedded_to_wmf property
articleTitle: use_emf_embedded_to_wmf property
second_title: Aspose.Words for Python
description: "MetafileRenderingOptions.use_emf_embedded_to_wmf property. Gets or sets a value determining how WMF metafiles with embedded EMF metafiles should be rendered."
type: docs
weight: 70
url: /sv/python-net/aspose.words.saving/metafilerenderingoptions/use_emf_embedded_to_wmf/
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
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF.
save_options = aw.saving.PdfSaveOptions()
# Ställ in egenskapen "EmfPlusDualRenderingMode" till "EmfPlusDualRenderingMode.Emf"
# för att endast rendera EMF-delen av en EMF+ dual metafil.
# Ställ in egenskapen "EmfPlusDualRenderingMode" till "EmfPlusDualRenderingMode.EmfPlus" för att
# rendera EMF+-delen av en EMF+ dual metafil.
# Ställ in egenskapen "EmfPlusDualRenderingMode" till "EmfPlusDualRenderingMode.EmfPlusWithFallback"
# för att rendera EMF+-delen av en EMF+ dual metafil om alla EMF+-poster stöds.
# Annars kommer Aspose.Words att rendera EMF-delen.
save_options.metafile_rendering_options.emf_plus_dual_rendering_mode = rendering_mode
# Ställ in egenskapen "UseEmfEmbeddedToWmf" till "true" för att rendera inbäddad EMF-data
# för metafiler som vi kan rendera som vektorgrafik.
save_options.metafile_rendering_options.use_emf_embedded_to_wmf = True
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.RenderMetafile.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [MetafileRenderingOptions](../)

