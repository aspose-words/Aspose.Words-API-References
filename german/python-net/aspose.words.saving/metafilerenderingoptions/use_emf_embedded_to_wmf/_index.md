---
title: MetafileRenderingOptions.use_emf_embedded_to_wmf property
linktitle: use_emf_embedded_to_wmf property
articleTitle: use_emf_embedded_to_wmf property
second_title: Aspose.Words for Python
description: "MetafileRenderingOptions.use_emf_embedded_to_wmf property. Gets or sets a value determining how WMF metafiles with embedded EMF metafiles should be rendered."
type: docs
weight: 70
url: /de/python-net/aspose.words.saving/metafilerenderingoptions/use_emf_embedded_to_wmf/
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
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
save_options = aw.saving.PdfSaveOptions()
# Setzen Sie die Eigenschaft "EmfPlusDualRenderingMode" auf "EmfPlusDualRenderingMode.Emf"
# um nur den EMF‑Teil einer EMF+‑Dual‑Metadatei zu rendern.
# Setzen Sie die Eigenschaft "EmfPlusDualRenderingMode" auf "EmfPlusDualRenderingMode.EmfPlus", um
# den EMF+‑Teil einer EMF+‑Dual‑Metadatei zu rendern.
# Setzen Sie die Eigenschaft "EmfPlusDualRenderingMode" auf "EmfPlusDualRenderingMode.EmfPlusWithFallback"
# um den EMF+ Teil einer EMF+ Dual-Metadatei zu rendern, falls alle EMF+‑Einträge unterstützt werden.
# Andernfalls wird Aspose.Words den EMF‑Teil rendern.
save_options.metafile_rendering_options.emf_plus_dual_rendering_mode = rendering_mode
# Setzen Sie die Eigenschaft "UseEmfEmbeddedToWmf" auf "true", um eingebettete EMF‑Daten zu rendern
# für Metadateien, die wir als Vektorgrafiken rendern können.
save_options.metafile_rendering_options.use_emf_embedded_to_wmf = True
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.RenderMetafile.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [MetafileRenderingOptions](../)

