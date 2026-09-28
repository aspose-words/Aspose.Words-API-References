---
title: EmfPlusDualRenderingMode enumeration
linktitle: EmfPlusDualRenderingMode enumeration
articleTitle: EmfPlusDualRenderingMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.EmfPlusDualRenderingMode enumeration. Specifies how Aspose.Words should render EMF+ Dual metafiles."
type: docs
weight: 160
url: /de/python-net/aspose.words.saving/emfplusdualrenderingmode/
---

## EmfPlusDualRenderingMode enumeration

Specifies how Aspose.Words should render EMF+ Dual metafiles.


### Members

| Name | Description |
| --- | --- |
| EMF_PLUS_WITH_FALLBACK | Aspose.Words tries to render EMF+ part of EMF+ Dual metafile. If some of the EMF+ records are not supported then Aspose.Words renders EMF part of EMF+ Dual metafile. |
| EMF_PLUS | Aspose.Words renders EMF+ part of EMF+ Dual metafile. |
| EMF | Aspose.Words renders EMF part of EMF+ Dual metafile. |

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

* module [aspose.words.saving](../)

