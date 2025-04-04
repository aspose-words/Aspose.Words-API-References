---
title: PlainTextDocument.builtInDocumentProperties property
linktitle: builtInDocumentProperties property
articleTitle: builtInDocumentProperties property
second_title: Aspose.Words for Node.js
description: "PlainTextDocument.builtInDocumentProperties property. Gets [PlainTextDocument.builtInDocumentProperties](./) of the document."
type: docs
weight: 20
url: /nodejs-net/aspose.words/plaintextdocument/builtInDocumentProperties/
---

## PlainTextDocument.builtInDocumentProperties property

Gets [PlainTextDocument.builtInDocumentProperties](./) of the document.



```js
get builtInDocumentProperties(): Aspose.Words.Properties.BuiltInDocumentProperties
```

### Examples

Shows how to load the contents of a Microsoft Word document in plaintext and then access the original document's built-in properties.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Hello world!");
doc.builtInDocumentProperties.author = "John Doe";

doc.save(base.artifactsDir + "PlainTextDocument.BuiltInProperties.docx");

let plaintext = new aw.PlainTextDocument(base.artifactsDir + "PlainTextDocument.BuiltInProperties.docx");

expect(plaintext.text.trim()).toEqual("Hello world!");
expect(plaintext.builtInDocumentProperties.author).toEqual("John Doe");
```

### See Also

* module [Aspose.Words](../../)
* class [PlainTextDocument](../)

