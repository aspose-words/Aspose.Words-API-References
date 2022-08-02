---
title: OdtSaveMeasureUnit enumeration
second_title: Aspose.Words for Python via .NET API Reference
description: "Specified units of measure to apply to measurable document content such as shape, widths and other during saving."
type: docs
weight: 450
url: /python-net/aspose.words.saving/odtsavemeasureunit/
---

## OdtSaveMeasureUnit enumeration

Specified units of measure to apply to measurable document content such as shape, widths and other during saving.


### Members

| Name | Description |
| --- | --- |
| CENTIMETERS | Specifies that the document content is saved using centimeters. |
| INCHES | Specifies that the document content is saved using inches. |

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

* module [aspose.words.saving](../)

