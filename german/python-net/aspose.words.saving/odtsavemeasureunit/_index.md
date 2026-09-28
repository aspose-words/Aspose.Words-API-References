---
title: OdtSaveMeasureUnit enumeration
linktitle: OdtSaveMeasureUnit enumeration
articleTitle: OdtSaveMeasureUnit enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.OdtSaveMeasureUnit enumeration. Specified units of measure to apply to measurable document content such as shape, widths and other during saving."
type: docs
weight: 530
url: /de/python-net/aspose.words.saving/odtsavemeasureunit/
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
# Wenn wir das Dokument nach .odt exportieren, können wir ein OdtSaveOptions‑Objekt verwenden, um zu ändern, wie wir das Dokument speichern.
# Wir können die Eigenschaft "MeasureUnit" auf "OdtSaveMeasureUnit.Centimeters" setzen
# um Inhalte wie Stilparameter im metrischen System zu definieren, das Open Office verwendet.
# Wir können die "MeasureUnit"-Eigenschaft auf "OdtSaveMeasureUnit.Inches" setzen
# um Inhalte wie Stilparameter mit dem imperialen System zu definieren, das Microsoft Word verwendet.
save_options = aw.saving.OdtSaveOptions()
save_options.measure_unit = odt_save_measure_unit
doc.save(file_name=ARTIFACTS_DIR + 'OdtSaveOptions.Odt11Schema.odt', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../)

