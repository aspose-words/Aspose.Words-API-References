---
title: RtfSaveOptions.saveFormat property
linktitle: saveFormat property
articleTitle: saveFormat property
second_title: Aspose.Words for Node.js
description: "RtfSaveOptions.saveFormat property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 40
url: /nodejs-net/aspose.words.saving/rtfsaveoptions/saveFormat/
---

## RtfSaveOptions.saveFormat property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.Rtf](../../../aspose.words/saveformat/#Rtf).



```js
get saveFormat(): Aspose.Words.SaveFormat
```

### Examples

Shows how to save a document to .rtf with custom options.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

// Create an "RtfSaveOptions" object to pass to the document's "Save" method to modify how we save it to an RTF.
let options = new aw.Saving.RtfSaveOptions();

expect(options.saveFormat).toEqual(aw.SaveFormat.Rtf);

// Set the "ExportCompactSize" property to "true" to
// reduce the saved document's size at the cost of right-to-left text compatibility.
options.exportCompactSize = true;

// Set the "ExportImagesFotOldReaders" property to "true" to use extra keywords to ensure that our document is
// compatible with pre-Microsoft Word 97 readers and WordPad.
// Set the "ExportImagesFotOldReaders" property to "false" to reduce the size of the document,
// but prevent old readers from being able to read any non-metafile or BMP images that the document may contain.
options.exportImagesForOldReaders = exportImagesForOldReaders;

doc.save(base.artifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [RtfSaveOptions](../)

