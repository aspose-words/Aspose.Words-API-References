---
title: SaveOptions.dml_rendering_mode property
linktitle: dml_rendering_mode property
articleTitle: dml_rendering_mode property
second_title: Aspose.Words for Python
description: "SaveOptions.dml_rendering_mode property. Gets or sets a value determining how DrawingML shapes are rendered."
type: docs
weight: 50
url: /ru/python-net/aspose.words.saving/saveoptions/dml_rendering_mode/
---

## SaveOptions.dml_rendering_mode property

Gets or sets a value determining how DrawingML shapes are rendered.


```python
@property
def dml_rendering_mode(self) -> aspose.words.saving.DmlRenderingMode:
    ...

@dml_rendering_mode.setter
def dml_rendering_mode(self, value: aspose.words.saving.DmlRenderingMode):
    ...

```

### Remarks

The default value is [DmlRenderingMode.FALLBACK](../../dmlrenderingmode/#FALLBACK).
This property is used when the document is exported to fixed page formats.




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

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

