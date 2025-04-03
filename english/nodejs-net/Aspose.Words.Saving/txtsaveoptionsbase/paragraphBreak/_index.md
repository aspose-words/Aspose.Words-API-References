---
title: TxtSaveOptionsBase.paragraphBreak property
linktitle: paragraphBreak property
articleTitle: paragraphBreak property
second_title: Aspose.Words for NodeJs
description: "TxtSaveOptionsBase.paragraphBreak property. Specifies the string to use as a paragraph break when exporting in text formats."
type: docs
weight: 40
url: /nodejs-net/aspose.words.saving/txtsaveoptionsbase/paragraphBreak/
---

## TxtSaveOptionsBase.paragraphBreak property

Specifies the string to use as a paragraph break when exporting in text formats.


```js
get paragraphBreak(): string
```

### Remarks

The default value is Aspose.Words.ControlChar.CrLf.




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
* class [TxtSaveOptionsBase](../)

