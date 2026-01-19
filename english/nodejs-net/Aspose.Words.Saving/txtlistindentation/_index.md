---
title: TxtListIndentation class
linktitle: TxtListIndentation class
articleTitle: TxtListIndentation class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.TxtListIndentation class. Specifies how list levels are indented when document is exporting to [SaveFormat.Text](../../aspose.words/saveformat/#Text) format"
type: docs
weight: 860
url: /nodejs-net/aspose.words.saving/txtlistindentation/
---

## TxtListIndentation class

Specifies how list levels are indented when document is exporting to [SaveFormat.Text](../../aspose.words/saveformat/#Text) format.
To learn more, visit the [Save a Document](https://docs.aspose.com/words/nodejs-net/save-a-document/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [TxtListIndentation()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [character](./character/) | Gets or sets which character to use for indenting list levels. The default value is '\\0', that means there is no indentation. |
| [count](./count/) | Gets or sets how many [TxtListIndentation.character](./character/) to use as indentation per one list level. The default value is 0, that means no indentation. |

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

* module [Aspose.Words.Saving](../)

