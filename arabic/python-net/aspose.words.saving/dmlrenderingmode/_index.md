---
title: DmlRenderingMode enumeration
linktitle: DmlRenderingMode enumeration
articleTitle: DmlRenderingMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.DmlRenderingMode enumeration. Specifies how DrawingML shapes are rendered to fixed page formats."
type: docs
weight: 90
url: /ar/python-net/aspose.words.saving/dmlrenderingmode/
---

## DmlRenderingMode enumeration

Specifies how DrawingML shapes are rendered to fixed page formats.


### Members

| Name | Description |
| --- | --- |
| FALLBACK | If fall-back shape is available for DrawingML, Aspose.Words renders fall-back shape instead of the DrawingML. |
| DRAWING_ML | Aspose.Words ignores fall-back shape of DrawingML and renders DrawingML itself. This is the default mode. |

### Examples

Shows how to configure the rendering quality of DrawingML effects in a document as we save it to PDF.

```python
doc = aw.Document(file_name=MY_DIR + 'DrawingML shape effects.docx')
# أنشئ كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .PDF.
options = aw.saving.PdfSaveOptions()
# اضبط خاصية "DmlEffectsRenderingMode" إلى "DmlEffectsRenderingMode.None" لتجاهل جميع تأثيرات DrawingML.
# اضبط خاصية "DmlEffectsRenderingMode" إلى "DmlEffectsRenderingMode.Simplified"
# لإظهار نسخة مبسطة من تأثيرات DrawingML.
# اضبط خاصية "DmlEffectsRenderingMode" إلى "DmlEffectsRenderingMode.Fine" لت
# عرض تأثيرات DrawingML بدقة أعلى وكذلك بتكلفة معالجة أكبر.
options.dml_effects_rendering_mode = effects_rendering_mode
self.assertEqual(aw.saving.DmlRenderingMode.DRAWING_ML, options.dml_rendering_mode)
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DrawingMLEffects.pdf', save_options=options)
```

Shows how to render fallback shapes when saving to PDF.

```python
doc = aw.Document(file_name=MY_DIR + 'DrawingML shape fallbacks.docx')
# أنشئ كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .PDF.
options = aw.saving.PdfSaveOptions()
# اضبط خاصية "DmlRenderingMode" إلى "DmlRenderingMode.Fallback"
# لإستبدال أشكال DML بأشكالها الاحتياطية.
# عيّن الخاصية "DmlRenderingMode" إلى "DmlRenderingMode.DrawingML"
# لإظهار أشكال DML نفسها.
options.dml_rendering_mode = dml_rendering_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DrawingMLFallback.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

