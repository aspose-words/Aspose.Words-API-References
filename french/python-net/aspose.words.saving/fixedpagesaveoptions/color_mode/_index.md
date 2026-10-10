---
title: FixedPageSaveOptions.color_mode property
linktitle: color_mode property
articleTitle: color_mode property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.color_mode property. Gets or sets a value determining how colors are rendered."
type: docs
weight: 10
url: /fr/python-net/aspose.words.saving/fixedpagesaveoptions/color_mode/
---

## FixedPageSaveOptions.color_mode property

Gets or sets a value determining how colors are rendered.


```python
@property
def color_mode(self) -> aspose.words.saving.ColorMode:
    ...

@color_mode.setter
def color_mode(self, value: aspose.words.saving.ColorMode):
    ...

```

### Remarks

The default value is [ColorMode.NORMAL](../../colormode/#NORMAL).



### Examples

Shows how to change image color with saving options property.

```python
doc = aw.Document(file_name=MY_DIR + 'Images.docx')
# Créez un objet "PdfSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
# pour modifier la façon dont cette méthode convertit le document en .PDF.
# Définissez la propriété "ColorMode" à "Grayscale" pour rendre toutes les images du document en noir et blanc.
# La taille du document de sortie peut être plus grande avec ce réglage.
# Définissez la propriété "ColorMode" à "Normal" pour rendre toutes les images en couleur.
pdf_save_options = aw.saving.PdfSaveOptions()
pdf_save_options.color_mode = color_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ColorRendering.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

