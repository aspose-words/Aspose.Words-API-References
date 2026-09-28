---
title: MetafileRenderingOptions.emf_plus_dual_rendering_mode property
linktitle: emf_plus_dual_rendering_mode property
articleTitle: emf_plus_dual_rendering_mode property
second_title: Aspose.Words for Python
description: "MetafileRenderingOptions.emf_plus_dual_rendering_mode property. Gets or sets a value determining how EMF+ Dual metafiles should be rendered."
type: docs
weight: 20
url: /de/python-net/aspose.words.saving/metafilerenderingoptions/emf_plus_dual_rendering_mode/
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

