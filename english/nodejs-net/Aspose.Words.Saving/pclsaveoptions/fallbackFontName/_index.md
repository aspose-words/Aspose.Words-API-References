---
title: PclSaveOptions.fallbackFontName property
linktitle: fallbackFontName property
articleTitle: fallbackFontName property
second_title: Aspose.Words for NodeJs
description: "PclSaveOptions.fallbackFontName property. Name of the font that will be used if no expected font is found in printer and built-in fonts collections."
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.Saving/pclsaveoptions/fallbackFontName/
---

## PclSaveOptions.fallbackFontName property

Name of the font that will be used
if no expected font is found in printer and built-in fonts collections.


```js
get fallbackFontName(): string
```

### Remarks

If no fallback is found, a warning is generated and "Arial" font is used.


### Examples

Shows how to declare a font that a printer will apply to printed text as a substitute should its original font be unavailable.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.font.name = "Non-existent font";
builder.write("Hello world!");

let saveOptions = new aw.Saving.PclSaveOptions();
saveOptions.fallbackFontName = "Times New Roman";

// This document will instruct the printer to apply "Times New Roman" to the text with the missing font.
// Should "Times New Roman" also be unavailable, the printer will default to the "Arial" font.
doc.save(base.artifactsDir + "PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PclSaveOptions](../)

