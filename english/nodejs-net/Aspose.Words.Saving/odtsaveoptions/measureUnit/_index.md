---
title: OdtSaveOptions.measureUnit property
linktitle: measureUnit property
articleTitle: measureUnit property
second_title: Aspose.Words for NodeJs
description: "OdtSaveOptions.measureUnit property. Allows to specify units of measure to apply to document content"
type: docs
weight: 40
url: /nodejs-net/Aspose.Words.Saving/odtsaveoptions/measureUnit/
---

## OdtSaveOptions.measureUnit property

Allows to specify units of measure to apply to document content.
The default value is [OdtSaveMeasureUnit.Centimeters](../../odtsavemeasureunit/#Centimeters)



```js
get measureUnit(): Aspose.Words.Saving.OdtSaveMeasureUnit
```

### Remarks

Open Office uses centimeters when specifying lengths, widths and other measurable formatting and
content properties in documents whereas MS Office uses inches.


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

* module [Aspose.Words.Saving](../../)
* class [OdtSaveOptions](../)

