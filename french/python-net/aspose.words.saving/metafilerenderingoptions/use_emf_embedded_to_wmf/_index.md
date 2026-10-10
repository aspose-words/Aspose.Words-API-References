---
title: MetafileRenderingOptions.use_emf_embedded_to_wmf property
linktitle: use_emf_embedded_to_wmf property
articleTitle: use_emf_embedded_to_wmf property
second_title: Aspose.Words for Python
description: "MetafileRenderingOptions.use_emf_embedded_to_wmf property. Gets or sets a value determining how WMF metafiles with embedded EMF metafiles should be rendered."
type: docs
weight: 70
url: /fr/python-net/aspose.words.saving/metafilerenderingoptions/use_emf_embedded_to_wmf/
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

* module [aspose.words.saving](../../)
* class [MetafileRenderingOptions](../)

