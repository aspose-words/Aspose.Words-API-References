---
title: OdtSaveOptions.measure_unit property
linktitle: measure_unit property
articleTitle: measure_unit property
second_title: Aspose.Words for Python
description: "OdtSaveOptions.measure_unit property. Allows to specify units of measure to apply to document content"
type: docs
weight: 40
url: /fr/python-net/aspose.words.saving/odtsaveoptions/measure_unit/
---

## OdtSaveOptions.measure_unit property

Allows to specify units of measure to apply to document content.
The default value is [OdtSaveMeasureUnit.CENTIMETERS](../../odtsavemeasureunit/#CENTIMETERS)



```python
@property
def measure_unit(self) -> aspose.words.saving.OdtSaveMeasureUnit:
    ...

@measure_unit.setter
def measure_unit(self, value: aspose.words.saving.OdtSaveMeasureUnit):
    ...

```

### Remarks

Open Office uses centimeters when specifying lengths, widths and other measurable formatting and
content properties in documents whereas MS Office uses inches.


### Examples

Shows how to make a saved document conform to an older ODT schema.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
save_options = aw.saving.OdtSaveOptions()
save_options.measure_unit = aw.saving.OdtSaveMeasureUnit.CENTIMETERS
save_options.is_strict_schema11 = export_to_odt_11_specs
doc.save(file_name=ARTIFACTS_DIR + 'OdtSaveOptions.Odt11Schema.odt', save_options=save_options)
doc = aw.Document(file_name=ARTIFACTS_DIR + 'OdtSaveOptions.Odt11Schema.odt')
self.assertEqual(aw.MeasurementUnits.CENTIMETERS, doc.layout_options.revision_options.measurement_unit)
```

Shows how to use different measurement units to define style parameters of a saved ODT document.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# Lorsque nous exportons le document au format .odt, nous pouvons utiliser un objet OdtSaveOptions pour modifier la façon dont nous enregistrons le document.
# Nous pouvons définir la propriété "MeasureUnit" sur "OdtSaveMeasureUnit.Centimeters"
# pour définir le contenu tel que les paramètres de style en utilisant le système métrique, que Open Office utilise.
# Nous pouvons définir la propriété "MeasureUnit" sur "OdtSaveMeasureUnit.Inches"
# pour définir le contenu tel que les paramètres de style en utilisant le système impérial, que Microsoft Word utilise.
save_options = aw.saving.OdtSaveOptions()
save_options.measure_unit = odt_save_measure_unit
doc.save(file_name=ARTIFACTS_DIR + 'OdtSaveOptions.Odt11Schema.odt', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OdtSaveOptions](../)

