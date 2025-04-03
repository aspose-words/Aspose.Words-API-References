---
title: RtfSaveOptions.exportCompactSize property
linktitle: exportCompactSize property
articleTitle: exportCompactSize property
second_title: Aspose.Words for NodeJs
description: "RtfSaveOptions.exportCompactSize property. Allows to make output RTF documents smaller in size, but if they contain  RTL (right-to-left) text, it will not be displayed correctly."
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.Saving/rtfsaveoptions/exportCompactSize/
---

## RtfSaveOptions.exportCompactSize property

Allows to make output RTF documents smaller in size, but if they contain 
RTL (right-to-left) text, it will not be displayed correctly.

Default value is ``false``.



```js
get exportCompactSize(): boolean
```

### Remarks

If the document that you want to convert to RTF using Aspose.Words does not contain
right-to-left text in languages like Arabic, then you can set this option to ``true``
to reduce the size of the resulting RTF.




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

