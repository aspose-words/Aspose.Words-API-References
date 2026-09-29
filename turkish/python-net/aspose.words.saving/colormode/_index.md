---
title: ColorMode enumeration
linktitle: ColorMode enumeration
articleTitle: ColorMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.ColorMode enumeration. Specifies how colors are rendered."
type: docs
weight: 20
url: /tr/python-net/aspose.words.saving/colormode/
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
# "PdfSaveOptions" nesnesi oluşturun; bu nesneyi belgenin "Save" metoduna geçebiliriz
# bu yöntemin belgeyi .PDF'ye nasıl dönüştürdüğünü değiştirmek için.
# "ColorMode" özelliğini "Grayscale" olarak ayarlayın, böylece belgedeki tüm görseller siyah beyaz olarak işlenir.
# Bu ayar ile çıktı belgesinin boyutu daha büyük olabilir.
# "ColorMode" özelliğini "Normal" olarak ayarlayın, böylece tüm görseller renkli işlenir.
pdf_save_options = aw.saving.PdfSaveOptions()
pdf_save_options.color_mode = color_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ColorRendering.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../)

