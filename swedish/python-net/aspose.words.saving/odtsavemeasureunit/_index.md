---
title: OdtSaveMeasureUnit enumeration
linktitle: OdtSaveMeasureUnit enumeration
articleTitle: OdtSaveMeasureUnit enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.OdtSaveMeasureUnit enumeration. Specified units of measure to apply to measurable document content such as shape, widths and other during saving."
type: docs
weight: 530
url: /sv/python-net/aspose.words.saving/odtsavemeasureunit/
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
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# När vi exporterar dokumentet till .odt kan vi använda ett OdtSaveOptions‑objekt för att ändra hur vi sparar dokumentet.
# Vi kan ställa in egenskapen "MeasureUnit" till "OdtSaveMeasureUnit.Centimeters"
# för att definiera innehåll såsom stilparametrar med det metriska systemet, som Open Office använder.
# Vi kan sätta egenskapen "MeasureUnit" till "OdtSaveMeasureUnit.Inches"
# för att definiera innehåll såsom stilparametrar med det imperiska systemet, som Microsoft Word använder.
save_options = aw.saving.OdtSaveOptions()
save_options.measure_unit = odt_save_measure_unit
doc.save(file_name=ARTIFACTS_DIR + 'OdtSaveOptions.Odt11Schema.odt', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../)

