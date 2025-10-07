---
title: PdfSaveOptions.exportFloatingShapesAsInlineTag property
linktitle: exportFloatingShapesAsInlineTag property
articleTitle: exportFloatingShapesAsInlineTag property
second_title: Aspose.Words for Node.js
description: "PdfSaveOptions.exportFloatingShapesAsInlineTag property. Gets or sets a value determining whether floating shapes are exported as inline tags in the document structure."
type: docs
weight: 150
url: /nodejs-net/aspose.words.saving/pdfsaveoptions/exportFloatingShapesAsInlineTag/
---

## PdfSaveOptions.exportFloatingShapesAsInlineTag property

Gets or sets a value determining whether floating shapes are exported as inline tags in the document structure.


```js
get exportFloatingShapesAsInlineTag(): boolean
```

### Remarks

Default value is ``false`` and floating shapes will be exported as block-level tags,
placed after the paragraph in which they are anchored.

When the value is ``true`` floating shapes will be exported as inline tags,
placed within the paragraph where they are anchored.

This value is ignored when [PdfSaveOptions.exportDocumentStructure](../exportDocumentStructure/) is ``false``. 




### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

