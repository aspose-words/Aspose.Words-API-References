---
title: EmfPlusDualRenderingMode enumeration
linktitle: EmfPlusDualRenderingMode enumeration
articleTitle: EmfPlusDualRenderingMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.EmfPlusDualRenderingMode enumeration. Specifies how Aspose.Words should render EMF+ Dual metafiles."
type: docs
weight: 150
url: /python-net/aspose.words.saving/emfplusdualrenderingmode/
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
doc = aw.Document(MY_DIR + 'EMF.docx')
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
doc.save(ARTIFACTS_DIR + 'PdfSaveOptions.render_metafile.pdf', save_options)
```

### See Also

* module [aspose.words.saving](../)

