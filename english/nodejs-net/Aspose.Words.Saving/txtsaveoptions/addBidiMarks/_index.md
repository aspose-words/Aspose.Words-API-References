---
title: TxtSaveOptions.addBidiMarks property
linktitle: addBidiMarks property
articleTitle: addBidiMarks property
second_title: Aspose.Words for NodeJs
description: "TxtSaveOptions.addBidiMarks property. Specifies whether to add bi-directional marks before each BiDi run when exporting in plain text format."
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.Saving/txtsaveoptions/addBidiMarks/
---

## TxtSaveOptions.addBidiMarks property

Specifies whether to add bi-directional marks before each BiDi run when exporting in plain text format.

The default value is ``false``.




```js
get addBidiMarks(): boolean
```

### Examples

Shows how to insert Unicode Character 'RIGHT-TO-LEFT MARK' (U+200F) before each bi-directional Run in text.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Hello world!");
builder.paragraphFormat.bidi = true;
builder.writeln("שלום עולם!");
builder.writeln("مرحبا بالعالم!");

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
// to modify how we save the document to plaintext.
let saveOptions = new aw.Saving.TxtSaveOptions();
saveOptions.encoding = "UTF-16";

// Set the "AddBidiMarks" property to "true" to add marks before runs
// with right-to-left text to indicate the fact.
// Set the "AddBidiMarks" property to "false" to write all left-to-right
// and right-to-left run equally with nothing to indicate which is which.
saveOptions.addBidiMarks = addBidiMarks;

doc.save(base.artifactsDir + "TxtSaveOptions.addBidiMarks.txt", saveOptions);

let docText = readTextFile(base.artifactsDir + "TxtSaveOptions.addBidiMarks.txt", false, "utf16le"); 

if (addBidiMarks)
{
  expect(docText).toEqual("\uFEFFHello world!‎\r\nשלום עולם!‏\r\nمرحبا بالعالم!‏\r\n\r\n");
  expect(docText.includes("\u200f")).toEqual(true);
}
else
{
  expect(docText).toEqual("\uFEFFHello world!\r\nשלום עולם!\r\nمرحبا بالعالم!\r\n\r\n");
  expect(docText.includes("\u200f")).toEqual(false);
}
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [TxtSaveOptions](../)

