---
title: OdtSaveOptions.isStrictSchema11 property
linktitle: isStrictSchema11 property
articleTitle: isStrictSchema11 property
second_title: Aspose.Words for NodeJs
description: "OdtSaveOptions.isStrictSchema11 property. Specifies whether export should correspond to ODT specification 1.1 strictly"
type: docs
weight: 30
url: /nodejs-net/Aspose.Words.Saving/odtsaveoptions/isStrictSchema11/
---

## OdtSaveOptions.isStrictSchema11 property

Specifies whether export should correspond to ODT specification 1.1 strictly.
OOo 3.0 displays files correctly when they contain elements and attributes of ODT 1.2.
Use "false" for this purpose, or "true" for strict conformity of specification 1.1.
The default value is ``false``.



```js
get isStrictSchema11(): boolean
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

* module [Aspose.Words.Saving](../../)
* class [OdtSaveOptions](../)

