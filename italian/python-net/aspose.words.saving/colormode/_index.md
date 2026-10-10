---
title: ColorMode enumeration
linktitle: ColorMode enumeration
articleTitle: ColorMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.ColorMode enumeration. Specifies how colors are rendered."
type: docs
weight: 20
url: /it/python-net/aspose.words.saving/colormode/
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
# Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
# per modificare il modo in cui quel metodo converte il documento in .PDF.
# Imposta la proprietà "ColorMode" a "Grayscale" per rendere tutte le immagini del documento in bianco e nero.
# La dimensione del documento di output potrebbe essere più grande con questa impostazione.
# Imposta la proprietà "ColorMode" a "Normal" per rendere tutte le immagini a colori.
pdf_save_options = aw.saving.PdfSaveOptions()
pdf_save_options.color_mode = color_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ColorRendering.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../)

