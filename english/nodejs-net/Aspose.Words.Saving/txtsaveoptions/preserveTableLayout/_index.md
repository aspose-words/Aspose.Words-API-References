---
title: TxtSaveOptions.preserveTableLayout property
linktitle: preserveTableLayout property
articleTitle: preserveTableLayout property
second_title: Aspose.Words for NodeJs
description: "TxtSaveOptions.preserveTableLayout property. Specifies whether the program should attempt to preserve layout of tables when saving in the plain text format"
type: docs
weight: 50
url: /nodejs-net/aspose.words.saving/txtsaveoptions/preserveTableLayout/
---

## TxtSaveOptions.preserveTableLayout property

Specifies whether the program should attempt to preserve layout of tables when saving in the plain text format.
The default value is ``false``.



```js
get preserveTableLayout(): boolean
```

### Examples

Shows how to preserve the layout of tables when converting to plaintext.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.startTable();
builder.insertCell();
builder.write("Row 1, cell 1");
builder.insertCell();
builder.write("Row 1, cell 2");
builder.endRow();
builder.insertCell();
builder.write("Row 2, cell 1");
builder.insertCell();
builder.write("Row 2, cell 2");
builder.endTable();

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
// to modify how we save the document to plaintext.
let txtSaveOptions = new aw.Saving.TxtSaveOptions();

// Set the "PreserveTableLayout" property to "true" to apply whitespace padding to the contents
// of the output plaintext document to preserve as much of the table's layout as possible.
// Set the "PreserveTableLayout" property to "false" to save all tables' contents
// as a continuous body of text, with just a new line for each row.
txtSaveOptions.preserveTableLayout = preserveTableLayout;

doc.save(base.artifactsDir + "TxtSaveOptions.preserveTableLayout.txt", txtSaveOptions);

let docText = readTextFile(base.artifactsDir + "TxtSaveOptions.preserveTableLayout.txt");
console.log(docText);

if (preserveTableLayout)
  expect(docText).toEqual("Row 1, cell 1                                           Row 1, cell 2\r\n" +
                          "Row 2, cell 1                                           Row 2, cell 2\r\n\r\n");
else
  expect(docText).toEqual("Row 1, cell 1\r" +
                          "Row 1, cell 2\r" +
                          "Row 2, cell 1\r" +
                          "Row 2, cell 2\r\r\n");
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [TxtSaveOptions](../)

