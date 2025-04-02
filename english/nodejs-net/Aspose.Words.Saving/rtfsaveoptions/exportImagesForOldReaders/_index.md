---
title: RtfSaveOptions.exportImagesForOldReaders property
linktitle: exportImagesForOldReaders property
articleTitle: exportImagesForOldReaders property
second_title: Aspose.Words for NodeJs
description: "RtfSaveOptions.exportImagesForOldReaders property. Specifies whether the keywords for old readers are written to RTF or not"
type: docs
weight: 30
url: /nodejs-net/Aspose.Words.Saving/rtfsaveoptions/exportImagesForOldReaders/
---

## RtfSaveOptions.exportImagesForOldReaders property

Specifies whether the keywords for "old readers" are written to RTF or not.
This can significantly affect the size of the RTF document.

Default value is ``True``.



```js
get exportImagesForOldReaders(): boolean
```

### Remarks

"Old readers" are pre-Microsoft Word 97 applications and also WordPad.
When this option is ``True`` Aspose.Words writes additional RTF keywords.
These keywords allow the document to be displayed correctly when opened in an 
"old reader" application, but can significantly increase the size of the document.

If you set this option to ``False``, then only images in WMF, EMF and BMP formats
will be displayed in "old readers".




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

