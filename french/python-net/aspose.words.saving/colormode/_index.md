---
title: ColorMode enumeration
linktitle: ColorMode enumeration
articleTitle: ColorMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.ColorMode enumeration. Specifies how colors are rendered."
type: docs
weight: 20
url: /fr/python-net/aspose.words.saving/colormode/
---

## ColorMode enumeration

Specifies how colors are rendered.


### Members

| Name | Description |
| --- | --- |
| NORMAL | Rendering with unmodified colors. |
| GRAYSCALE | Rendering with colors in a range of gray shades from white to black. |

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

* module [aspose.words.saving](../)

