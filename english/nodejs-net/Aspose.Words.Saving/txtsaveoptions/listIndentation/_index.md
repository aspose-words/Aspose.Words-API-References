---
title: TxtSaveOptions.listIndentation property
linktitle: listIndentation property
articleTitle: listIndentation property
second_title: Aspose.Words for NodeJs
description: "TxtSaveOptions.listIndentation property. Gets a [TxtListIndentation](../../txtlistindentation/) object that specifies how many and which character to use for indentation of list levels"
type: docs
weight: 30
url: /nodejs-net/Aspose.Words.Saving/txtsaveoptions/listIndentation/
---

## TxtSaveOptions.listIndentation property

Gets a [TxtListIndentation](../../txtlistindentation/) object that specifies how many and which character to use for indentation of list levels.
By default it is zero count of character '\\0', that means no indentation.



```js
get listIndentation(): Aspose.Words.Saving.TxtListIndentation
```

### Examples

Shows how to configure list indenting when saving a document to plaintext.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Create a list with three levels of indentation.
builder.listFormat.applyNumberDefault();
builder.writeln("Item 1");
builder.listFormat.listIndent();
builder.writeln("Item 2");
builder.listFormat.listIndent(); 
builder.write("Item 3");

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
// to modify how we save the document to plaintext.
let txtSaveOptions = new aw.Saving.TxtSaveOptions();

// Set the "Character" property to assign a character to use
// for padding that simulates list indentation in plaintext.
txtSaveOptions.listIndentation.character = ' ';

// Set the "Count" property to specify the number of times
// to place the padding character for each list indent level.
txtSaveOptions.listIndentation.count = 3;

doc.save(base.artifactsDir + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

let docText = readTextFile(base.artifactsDir + "TxtSaveOptions.TxtListIndentation.txt");

expect(docText).toEqual("1. Item 1\r\n" +
                        "   a. Item 2\r\n" +
                        "      i. Item 3\r\n");
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [TxtSaveOptions](../)

