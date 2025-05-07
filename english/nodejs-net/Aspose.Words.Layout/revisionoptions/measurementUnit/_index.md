---
title: RevisionOptions.measurementUnit property
linktitle: measurementUnit property
articleTitle: measurementUnit property
second_title: Aspose.Words for Node.js
description: "RevisionOptions.measurementUnit property. Allows to specify the measurement units for revision comments"
type: docs
weight: 80
url: /nodejs-net/aspose.words.layout/revisionoptions/measurementUnit/
---

## RevisionOptions.measurementUnit property

Allows to specify the measurement units for revision comments.
Default value is [MeasurementUnits.Centimeters](../../../aspose.words/measurementunits/#Centimeters)



```js
get measurementUnit(): Aspose.Words.MeasurementUnits
```

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

* module [Aspose.Words.Layout](../../)
* class [RevisionOptions](../)

