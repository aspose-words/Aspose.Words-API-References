---
title: PdfSaveOptions.additionalTextPositioning property
linktitle: additionalTextPositioning property
articleTitle: additionalTextPositioning property
second_title: Aspose.Words for Node.js
description: "PdfSaveOptions.additionalTextPositioning property. A flag specifying whether to write additional text positioning operators or not."
type: docs
weight: 20
url: /nodejs-net/aspose.words.saving/pdfsaveoptions/additionalTextPositioning/
---

## PdfSaveOptions.additionalTextPositioning property

A flag specifying whether to write additional text positioning operators or not.


```js
get additionalTextPositioning(): boolean
```

### Remarks

If ``true``, additional text positioning operators are written to the output PDF. This may help to overcome
issues with inaccurate text positioning with some printers. The downside is the increased PDF document size.


The default value is ``false``.




### Examples

Show how to write additional text positioning operators.

```js
let doc = new aw.Document(base.myDir + "Text positioning operators.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let saveOptions = new aw.Saving.PdfSaveOptions();
saveOptions.textCompression = aw.Saving.PdfTextCompression.None;
// Set the "AdditionalTextPositioning" property to "true" to attempt to fix incorrect
// element positioning in the output PDF, should there be any, at the cost of increased file size.
// Set the "AdditionalTextPositioning" property to "false" to render the document as usual.
saveOptions.additionalTextPositioning = applyAdditionalTextPositioning;

doc.save(base.artifactsDir + "PdfSaveOptions.additionalTextPositioning.pdf", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

