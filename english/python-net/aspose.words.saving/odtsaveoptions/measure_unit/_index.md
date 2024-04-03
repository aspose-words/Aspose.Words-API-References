---
title: OdtSaveOptions.measure_unit property
linktitle: measure_unit property
articleTitle: measure_unit property
second_title: Aspose.Words for Python
description: "OdtSaveOptions.measure_unit property. Allows to specify units of measure to apply to document content"
type: docs
weight: 40
url: /python-net/aspose.words.saving/odtsaveoptions/measure_unit/
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

Shows how to use different measurement units to define style parameters of a saved ODT document.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

# When we export the document to .odt, we can use an OdtSaveOptions object to modify how we save the document.
# We can set the "measure_unit" property to "OdtSaveMeasureUnit.CENTIMETERS"
# to define content such as style parameters using the metric system, which Open Office uses.
# We can set the "measure_unit" property to "OdtSaveMeasureUnit.INCHES"
# to define content such as style parameters using the imperial system, which Microsoft Word uses.
save_options = aw.saving.OdtSaveOptions()
save_options.measure_unit = odt_save_measure_unit

doc.save(ARTIFACTS_DIR + "OdtSaveOptions.measurement_units.odt", save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OdtSaveOptions](../)

