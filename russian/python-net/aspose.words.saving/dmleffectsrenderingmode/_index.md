---
title: DmlEffectsRenderingMode enumeration
linktitle: DmlEffectsRenderingMode enumeration
articleTitle: DmlEffectsRenderingMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.DmlEffectsRenderingMode enumeration. Specifies how DrawingML effects are rendered to fixed page formats."
type: docs
weight: 80
url: /ru/python-net/aspose.words.saving/dmleffectsrenderingmode/
---

## DmlEffectsRenderingMode enumeration

Specifies how DrawingML effects are rendered to fixed page formats.


### Members

| Name | Description |
| --- | --- |
| SIMPLIFIED | Rendering of DrawingML effects are simplified. |
| NONE | No DrawingML effects are rendered. |
| FINE | DrawingML effects are rendered in fine mode which involves advanced processing. In this mode rendering of effects gives better results but at a higher performance cost than [DmlEffectsRenderingMode.SIMPLIFIED](./#SIMPLIFIED) mode. |

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

### See Also

* module [aspose.words.saving](../)

