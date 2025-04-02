---
title: PlainTextDocument.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for NodeJs
description: "PlainTextDocument.text property. Gets textual content of the document concatenated as a string."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words/plaintextdocument/text/
---

## PlainTextDocument.text property

Gets textual content of the document concatenated as a string.


```js
get text(): string
```

### Examples

Shows how to load the contents of a Microsoft Word document in plaintext.

```js
let doc = new aw.Document(); 
let builder = new aw.DocumentBuilder(doc);
builder.writeln("Hello world!");

doc.save(base.artifactsDir + "PlainTextDocument.load.docx");

let plaintext = new aw.PlainTextDocument(base.artifactsDir + "PlainTextDocument.load.docx");

expect(plaintext.text.trim()).toEqual("Hello world!");
```

### See Also

* module [Aspose.Words](../../)
* class [PlainTextDocument](../)

