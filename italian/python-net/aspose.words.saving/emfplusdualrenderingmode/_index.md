---
title: EmfPlusDualRenderingMode enumeration
linktitle: EmfPlusDualRenderingMode enumeration
articleTitle: EmfPlusDualRenderingMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.EmfPlusDualRenderingMode enumeration. Specifies how Aspose.Words should render EMF+ Dual metafiles."
type: docs
weight: 160
url: /it/python-net/aspose.words.saving/emfplusdualrenderingmode/
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
# Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
# per modificare il modo in cui quel metodo converte il documento in .PDF.
save_options = aw.saving.PdfSaveOptions()
# Imposta la proprietà "EmfPlusDualRenderingMode" a "EmfPlusDualRenderingMode.Emf"
# per rendere solo la parte EMF di un metafile duale EMF+.
# Imposta la proprietà "EmfPlusDualRenderingMode" a "EmfPlusDualRenderingMode.EmfPlus" per
# rendere la parte EMF+ di un metafile duale EMF+.
# Imposta la proprietà "EmfPlusDualRenderingMode" a "EmfPlusDualRenderingMode.EmfPlusWithFallback"
# per rendere la parte EMF+ di un metafile duale EMF+ se tutti i record EMF+ sono supportati.
# Altrimenti, Aspose.Words renderà la parte EMF.
save_options.metafile_rendering_options.emf_plus_dual_rendering_mode = rendering_mode
# Imposta la proprietà "UseEmfEmbeddedToWmf" a "true" per rendere i dati EMF incorporati
# per i metafili che possiamo rendere come grafica vettoriale.
save_options.metafile_rendering_options.use_emf_embedded_to_wmf = True
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.RenderMetafile.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../)

