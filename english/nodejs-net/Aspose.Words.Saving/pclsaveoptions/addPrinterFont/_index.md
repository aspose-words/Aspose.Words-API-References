---
title: PclSaveOptions.addPrinterFont method
linktitle: addPrinterFont method
articleTitle: addPrinterFont method
second_title: Aspose.Words for Node.js
description: "PclSaveOptions.addPrinterFont method. Adds information about font that is uploaded to the printer by manufacturer."
type: docs
weight: 50
url: /nodejs-net/aspose.words.saving/pclsaveoptions/addPrinterFont/
---

## addPrinterFont(fontFullName, fontPclName) {#string_string}

Adds information about font that is uploaded to the printer by manufacturer.


```js
addPrinterFont(fontFullName: string, fontPclName: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fontFullName | string | Full name of the font (e.g. "Times New Roman Bold Italic"). |
| fontPclName | string | Name of the font that is used in Pcl document. |

### Remarks

There are 52 fonts that are to be built in any printer according to Pcl specification.
However manufactures can add some other fonts to their devices.


### Examples

Shows how to get a printer to substitute all instances of a specific font with a different font.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.font.name = "Courier";
builder.write("Hello world!");

let saveOptions = new aw.Saving.PclSaveOptions();
saveOptions.addPrinterFont("Courier New", "Courier");

// When printing this document, the printer will use the "Courier New" font
// to access places where our document used the "Courier" font.
doc.save(base.artifactsDir + "PclSaveOptions.addPrinterFont.pcl", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PclSaveOptions](../)

