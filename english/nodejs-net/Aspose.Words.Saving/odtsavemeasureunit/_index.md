---
title: OdtSaveMeasureUnit enumeration
linktitle: OdtSaveMeasureUnit enumeration
articleTitle: OdtSaveMeasureUnit enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.OdtSaveMeasureUnit enumeration. Specified units of measure to apply to measurable document content such as shape, widths and other during saving."
type: docs
weight: 500
url: /nodejs-net/Aspose.Words.Saving/odtsavemeasureunit/
---

## OdtSaveMeasureUnit enumeration

Specified units of measure to apply to measurable document content such as shape, widths and other during saving.


### Members

| Name | Description |
| --- | --- |
| Centimeters | Specifies that the document content is saved using centimeters. |
| Inches | Specifies that the document content is saved using inches. |

### Examples

Shows how to use different measurement units to define style parameters of a saved ODT document.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

// When we export the document to .odt, we can use an OdtSaveOptions object to modify how we save the document.
// We can set the "MeasureUnit" property to "OdtSaveMeasureUnit.Centimeters"
// to define content such as style parameters using the metric system, which Open Office uses. 
// We can set the "MeasureUnit" property to "OdtSaveMeasureUnit.Inches"
// to define content such as style parameters using the imperial system, which Microsoft Word uses.
let saveOptions = new aw.Saving.OdtSaveOptions();
saveOptions.measureUnit = odtSaveMeasureUnit;

doc.save(base.artifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../)

