---
title: OdtSaveMeasureUnit enumeration
linktitle: OdtSaveMeasureUnit enumeration
articleTitle: OdtSaveMeasureUnit enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.OdtSaveMeasureUnit enumeration. Specified units of measure to apply to measurable document content such as shape, widths and other during saving."
type: docs
weight: 530
url: /fr/python-net/aspose.words.saving/odtsavemeasureunit/
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

* module [aspose.words.saving](../)

