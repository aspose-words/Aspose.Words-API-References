---
title: RevisionOptions.measurement_unit property
linktitle: measurement_unit property
articleTitle: measurement_unit property
second_title: Aspose.Words for Python
description: "RevisionOptions.measurement_unit property. Allows to specify the measurement units for revision comments"
type: docs
weight: 80
url: /python-net/aspose.words.layout/revisionoptions/measurement_unit/
---

## RevisionOptions.measurement_unit property

Allows to specify the measurement units for revision comments.
Default value is [MeasurementUnits.CENTIMETERS](../../../aspose.words/measurementunits/#CENTIMETERS)



```python
@property
def measurement_unit(self) -> aspose.words.MeasurementUnits:
    ...

@measurement_unit.setter
def measurement_unit(self, value: aspose.words.MeasurementUnits):
    ...

```

### Examples

Shows how to make a saved document conform to an older ODT schema.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
save_options = aw.saving.OdtSaveOptions()
save_options.measure_unit = aw.saving.OdtSaveMeasureUnit.CENTIMETERS
save_options.is_strict_schema11 = export_to_odt_11_specs
doc.save(file_name=ARTIFACTS_DIR + 'OdtSaveOptions.Odt11Schema.odt', save_options=save_options)
```

### See Also

* module [aspose.words.layout](../../)
* class [RevisionOptions](../)

