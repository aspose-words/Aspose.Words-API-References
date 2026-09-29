---
title: ColorMode enumeration
linktitle: ColorMode enumeration
articleTitle: ColorMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.ColorMode enumeration. Specifies how colors are rendered."
type: docs
weight: 20
url: /ru/python-net/aspose.words.saving/colormode/
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
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
# Установите свойство "ColorMode" в значение "Grayscale", чтобы отрисовывать все изображения из документа в чёрно‑белом режиме.
# Размер выходного документа может быть больше при этом параметре.
# Установите свойство "ColorMode" в значение "Normal", чтобы отрисовывать все изображения в цвете.
pdf_save_options = aw.saving.PdfSaveOptions()
pdf_save_options.color_mode = color_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ColorRendering.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../)

