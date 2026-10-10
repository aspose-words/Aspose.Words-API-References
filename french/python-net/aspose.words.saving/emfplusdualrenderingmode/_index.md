---
title: EmfPlusDualRenderingMode enumeration
linktitle: EmfPlusDualRenderingMode enumeration
articleTitle: EmfPlusDualRenderingMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.EmfPlusDualRenderingMode enumeration. Specifies how Aspose.Words should render EMF+ Dual metafiles."
type: docs
weight: 160
url: /fr/python-net/aspose.words.saving/emfplusdualrenderingmode/
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
# Créez un objet "PdfSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
# pour modifier la façon dont cette méthode convertit le document en .PDF.
save_options = aw.saving.PdfSaveOptions()
# Définissez la propriété "EmfPlusDualRenderingMode" à "EmfPlusDualRenderingMode.Emf"
# pour ne rendre que la partie EMF d'un métafichier EMF+ dual.
# Définissez la propriété "EmfPlusDualRenderingMode" à "EmfPlusDualRenderingMode.EmfPlus" pour
# rendre la partie EMF+ d'un métafichier EMF+ dual.
# Définissez la propriété "EmfPlusDualRenderingMode" à "EmfPlusDualRenderingMode.EmfPlusWithFallback"
# pour rendre la partie EMF+ d'un métafichier EMF+ dual si tous les enregistrements EMF+ sont pris en charge.
# Sinon, Aspose.Words rendra la partie EMF.
save_options.metafile_rendering_options.emf_plus_dual_rendering_mode = rendering_mode
# Définissez la propriété "UseEmfEmbeddedToWmf" à "true" pour rendre les données EMF intégrées
# pour les métafichiers que nous pouvons rendre en tant que graphiques vectoriels.
save_options.metafile_rendering_options.use_emf_embedded_to_wmf = True
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.RenderMetafile.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../)

