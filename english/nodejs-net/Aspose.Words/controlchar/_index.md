---
title: ControlChar class
linktitle: ControlChar class
articleTitle: ControlChar class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.ControlChar class. Control characters often encountered in documents"
type: docs
weight: 280
url: /nodejs-net/aspose.words/controlchar/
---

## ControlChar class

Control characters often encountered in documents.
To learn more, visit the [Working With Control Characters](https://docs.aspose.com/words/nodejs-net/working-with-control-characters/) documentation article.




### Remarks

Provides both char and string versions of the same constants. For example:
string Aspose.Words.ControlChar.LineBreak and char Aspose.Words.ControlChar.LineBreakChar have the same value.



### Examples

Shows how to use control characters.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert paragraphs with text with DocumentBuilder.
builder.writeln("Hello world!");
builder.writeln("Hello again!");

// Converting the document to text form reveals that control characters
// represent some of the document's structural elements, such as page breaks.
expect(doc.getText()).toEqual(`Hello world!${aw.ControlChar.cr}` +
                        `Hello again!${aw.ControlChar.cr}` +
                        aw.ControlChar.pageBreak);

// When converting a document to string form,
// we can omit some of the control characters with the Trim method.
expect(doc.getText().trim()).toEqual(`Hello world!${aw.ControlChar.cr}` +
                        "Hello again!");
```

### See Also

* module [Aspose.Words](../)

