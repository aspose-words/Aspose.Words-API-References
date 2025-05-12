---
title: TxtListIndentation.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Node.js
description: "TxtListIndentation.count property. Gets or sets how many [TxtListIndentation.character](../character/) to use as indentation per one list level"
type: docs
weight: 30
url: /nodejs-net/aspose.words.saving/txtlistindentation/count/
---

## TxtListIndentation.count property

Gets or sets how many [TxtListIndentation.character](../character/) to use as indentation per one list level.
The default value is 0, that means no indentation.



```js
get count(): number
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
const newLine = "\r\n";

expect(docText).toEqual(`1. Item 1${newLine}` +
                        `   a. Item 2${newLine}` +
                        `      i. Item 3${newLine}`);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [TxtListIndentation](../)

