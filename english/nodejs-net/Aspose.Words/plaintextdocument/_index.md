---
title: PlainTextDocument class
linktitle: PlainTextDocument class
articleTitle: PlainTextDocument class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.PlainTextDocument class. Allows to extract plain-text representation of the document's content"
type: docs
weight: 1060
url: /nodejs-net/aspose.words/plaintextdocument/
---

## PlainTextDocument class

Allows to extract plain-text representation of the document's content.
To learn more, visit the [Working with Text Document](https://docs.aspose.com/words/nodejs-net/working-with-text-document/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [PlainTextDocument(fileName)](./constructor/#string) | Creates a plain text document from a file. Automatically detects the file format. |
| [PlainTextDocument(fileName, loadOptions)](./constructor/#string_loadoptions) | Creates a plain text document from a file. Allows to specify additional options such as an encryption password. |
| [PlainTextDocument(stream)](./constructor/#buffer) | Creates a plain text document from a stream. Automatically detects the file format. |
| [PlainTextDocument(stream, loadOptions)](./constructor/#buffer_loadoptions) | Creates a plain text document from a stream. Allows to specify additional options such as an encryption password. |

### Properties

| Name | Description |
| --- | --- |
| [builtInDocumentProperties](./builtInDocumentProperties/) | Gets [PlainTextDocument.builtInDocumentProperties](./builtInDocumentProperties/) of the document. |
| [customDocumentProperties](./customDocumentProperties/) | Gets [PlainTextDocument.customDocumentProperties](./customDocumentProperties/) of the document. |
| [text](./text/) | Gets textual content of the document concatenated as a string. |

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

* module [Aspose.Words](../)

