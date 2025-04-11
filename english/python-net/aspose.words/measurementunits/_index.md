---
title: MeasurementUnits enumeration
linktitle: MeasurementUnits enumeration
articleTitle: MeasurementUnits enumeration
second_title: Aspose.Words for Python
description: "aspose.words.MeasurementUnits enumeration. Specifies the unit of measurement."
type: docs
weight: 720
url: /python-net/aspose.words/measurementunits/
---

## MeasurementUnits enumeration

Specifies the unit of measurement.


### Members

| Name | Description |
| --- | --- |
| INCHES | Inches. |
| CENTIMETERS | Centimeters. |
| MILLIMETERS | Millimeters. |
| POINTS | Points. |
| PICAS | Picas (commonly used in traditional typewriter font spacing). |

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

* module [aspose.words](../)

