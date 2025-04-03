---
title: PlainTextDocument.customDocumentProperties property
linktitle: customDocumentProperties property
articleTitle: customDocumentProperties property
second_title: Aspose.Words for NodeJs
description: "PlainTextDocument.customDocumentProperties property. Gets [PlainTextDocument.customDocumentProperties](./) of the document."
type: docs
weight: 30
url: /nodejs-net/aspose.words/plaintextdocument/customDocumentProperties/
---

## PlainTextDocument.customDocumentProperties property

Gets [PlainTextDocument.customDocumentProperties](./) of the document.



```js
get customDocumentProperties(): Aspose.Words.Properties.CustomDocumentProperties
```

### Examples

Shows how to load the contents of a Microsoft Word document in plaintext and then access the original document's custom properties.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Hello world!");
doc.customDocumentProperties.add("Location of writing", "123 Main St, London, UK");

doc.save(base.artifactsDir + "PlainTextDocument.customDocumentProperties.docx");

let plaintext = new aw.PlainTextDocument(base.artifactsDir + "PlainTextDocument.customDocumentProperties.docx");

expect(plaintext.text.trim()).toEqual("Hello world!");
expect(plaintext.customDocumentProperties.at("Location of writing").toString()).toEqual("123 Main St, London, UK");
```

### See Also

* module [Aspose.Words](../../)
* class [PlainTextDocument](../)

