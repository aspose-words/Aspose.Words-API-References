---
title: DmlRenderingMode enumeration
linktitle: DmlRenderingMode enumeration
articleTitle: DmlRenderingMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.DmlRenderingMode enumeration. Specifies how DrawingML shapes are rendered to fixed page formats."
type: docs
weight: 90
url: /ru/python-net/aspose.words.saving/dmlrenderingmode/
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
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
options = aw.saving.PdfSaveOptions()
# Установите свойство "DmlEffectsRenderingMode" в "DmlEffectsRenderingMode.None", чтобы удалить все эффекты DrawingML.
# Установите свойство "DmlEffectsRenderingMode" в "DmlEffectsRenderingMode.Simplified"
# чтобы отобразить упрощённую версию эффектов DrawingML.
# Установите свойство "DmlEffectsRenderingMode" в "DmlEffectsRenderingMode.Fine", чтобы
# отображать эффекты DrawingML с большей точностью, но и с более высокими затратами на обработку.
options.dml_effects_rendering_mode = effects_rendering_mode
self.assertEqual(aw.saving.DmlRenderingMode.DRAWING_ML, options.dml_rendering_mode)
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DrawingMLEffects.pdf', save_options=options)
```

Shows how to render fallback shapes when saving to PDF.

```python
doc = aw.Document(file_name=MY_DIR + 'DrawingML shape fallbacks.docx')
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
options = aw.saving.PdfSaveOptions()
# Установите свойство "DmlRenderingMode" в "DmlRenderingMode.Fallback"
# чтобы заменить формы DML их резервными формами.
# Установите свойство "DmlRenderingMode" в значение "DmlRenderingMode.DrawingML"
# чтобы отрисовать сами формы DML.
options.dml_rendering_mode = dml_rendering_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DrawingMLFallback.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

