---
title: SaveOptions.memoryOptimization property
linktitle: memoryOptimization property
articleTitle: memoryOptimization property
second_title: Aspose.Words for Node.js
description: "SaveOptions.memoryOptimization property. Gets or sets value determining if memory optimization should be performed before saving the document"
type: docs
weight: 80
url: /nodejs-net/aspose.words.saving/saveoptions/memoryOptimization/
---

## SaveOptions.memoryOptimization property

Gets or sets value determining if memory optimization should be performed before saving the document.
Default value for this property is ``false``.



```js
get memoryOptimization(): boolean
```

### Remarks

Setting this option to ``true`` can significantly decrease memory consumption while saving large documents at the cost of slower saving time.



### Examples

Shows an option to optimize memory consumption when rendering large documents to PDF.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let saveOptions = aw.Saving.SaveOptions.createSaveOptions(aw.SaveFormat.Pdf);

// Set the "MemoryOptimization" property to "true" to lower the memory footprint of large documents' saving operations
// at the cost of increasing the duration of the operation.
// Set the "MemoryOptimization" property to "false" to save the document as a PDF normally.
saveOptions.memoryOptimization = memoryOptimization;

doc.save(base.artifactsDir + "PdfSaveOptions.memoryOptimization.pdf", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [SaveOptions](../)

