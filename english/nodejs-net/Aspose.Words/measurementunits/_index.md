---
title: MeasurementUnits enumeration
linktitle: MeasurementUnits enumeration
articleTitle: MeasurementUnits enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.MeasurementUnits enumeration. Specifies the unit of measurement."
type: docs
weight: 810
url: /nodejs-net/aspose.words/measurementunits/
---

## MeasurementUnits enumeration

Specifies the unit of measurement.


### Members

| Name | Description |
| --- | --- |
| Inches | Inches. |
| Centimeters | Centimeters. |
| Millimeters | Millimeters. |
| Points | Points. |
| Picas | Picas (commonly used in traditional typewriter font spacing). |

### Examples

Shows how to make a saved document conform to an older ODT schema.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

let saveOptions = new aw.Saving.OdtSaveOptions();
saveOptions.measureUnit = aw.Saving.OdtSaveMeasureUnit.Centimeters;
saveOptions.isStrictSchema11 = exportToOdt11Specs;

doc.save(base.artifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### See Also

* module [Aspose.Words](../)

