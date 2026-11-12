---
title: PdfSaveOptions.dml_effects_rendering_mode property
linktitle: dml_effects_rendering_mode property
articleTitle: dml_effects_rendering_mode property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.dml_effects_rendering_mode property. Gets or sets a value determining how DrawingML effects are rendered."
type: docs
weight: 100
url: /ru/python-net/aspose.words.saving/pdfsaveoptions/dml_effects_rendering_mode/
---

## PdfSaveOptions.dml_effects_rendering_mode property

Gets or sets a value determining how DrawingML effects are rendered.


```python
@property
def dml_effects_rendering_mode(self) -> aspose.words.saving.DmlEffectsRenderingMode:
    ...

@dml_effects_rendering_mode.setter
def dml_effects_rendering_mode(self, value: aspose.words.saving.DmlEffectsRenderingMode):
    ...

```

### Remarks

The default value is [DmlEffectsRenderingMode.SIMPLIFIED](../../dmleffectsrenderingmode/#SIMPLIFIED).
This property is used when the document is exported to fixed page formats.

If [PdfSaveOptions.compliance](../compliance/) is set to [PdfCompliance.PDF_A1A](../../pdfcompliance/#PDF_A1A) or [PdfCompliance.PDF_A1B](../../pdfcompliance/#PDF_A1B),
property always returns [DmlEffectsRenderingMode.NONE](../../dmleffectsrenderingmode/#NONE).




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

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

