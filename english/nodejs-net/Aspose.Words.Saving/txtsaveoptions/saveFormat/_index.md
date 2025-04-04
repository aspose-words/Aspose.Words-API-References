---
title: TxtSaveOptions.saveFormat property
linktitle: saveFormat property
articleTitle: saveFormat property
second_title: Aspose.Words for Node.js
description: "TxtSaveOptions.saveFormat property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 60
url: /nodejs-net/aspose.words.saving/txtsaveoptions/saveFormat/
---

## TxtSaveOptions.saveFormat property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.Text](../../../aspose.words/saveformat/#Text).



```js
get saveFormat(): Aspose.Words.SaveFormat
```

### Examples

Shows how to save a .txt document with a custom paragraph break.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Paragraph 1.");
builder.writeln("Paragraph 2.");
builder.write("Paragraph 3.");

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
// to modify how we save the document to plaintext.
let txtSaveOptions = new aw.Saving.TxtSaveOptions();

expect(txtSaveOptions.saveFormat).toEqual(aw.SaveFormat.Text);

// Set the "ParagraphBreak" to a custom value that we wish to put at the end of every paragraph.
txtSaveOptions.paragraphBreak = " End of paragraph.\n\n\t";

doc.save(base.artifactsDir + "TxtSaveOptions.paragraphBreak.txt", txtSaveOptions);

let docText = readTextFile(base.artifactsDir + "TxtSaveOptions.paragraphBreak.txt");

expect(docText).toEqual("Paragraph 1. End of paragraph.\n\n\t" +
                        "Paragraph 2. End of paragraph.\n\n\t" +
                        "Paragraph 3. End of paragraph.\n\n\t");
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [TxtSaveOptions](../)

