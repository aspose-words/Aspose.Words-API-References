---
title: ColorMode enumeration
linktitle: ColorMode enumeration
articleTitle: ColorMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.ColorMode enumeration. Specifies how colors are rendered."
type: docs
weight: 20
url: /ar/python-net/aspose.words.saving/colormode/
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
# أنشئ كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .PDF.
# قم بتعيين الخاصية "ColorMode" إلى "Grayscale" لعرض جميع الصور من المستند بالأبيض والأسود.
# قد يكون حجم المستند الناتج أكبر باستخدام هذا الإعداد.
# قم بتعيين الخاصية "ColorMode" إلى "Normal" لعرض جميع الصور بالألوان.
pdf_save_options = aw.saving.PdfSaveOptions()
pdf_save_options.color_mode = color_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ColorRendering.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../)

