---
title: PlainTextDocument.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "PlainTextDocument.text property. Gets textual content of the document concatenated as a string."
type: docs
weight: 40
url: /python-net/aspose.words/plaintextdocument/text/
---

## PlainTextDocument.text property

Gets textual content of the document concatenated as a string.


### Examples

Shows how to load the contents of a Microsoft Word document in plaintext.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln("Hello world!")

doc.save(ARTIFACTS_DIR + "PlainTextDocument.load.docx")

plaintext = aw.PlainTextDocument(ARTIFACTS_DIR + "PlainTextDocument.load.docx")

self.assertEqual("Hello world!", plaintext.text.strip())
```

### See Also

* module [aspose.words](../../)
* class [PlainTextDocument](../)

