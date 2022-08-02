---
title: custom_document_properties property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets [PlainTextDocument.custom_document_properties](./) of the document."
type: docs
weight: 30
url: /python-net/aspose.words/plaintextdocument/custom_document_properties/
---

## PlainTextDocument.custom_document_properties property

Gets [PlainTextDocument.custom_document_properties](./) of the document.



### Examples

Shows how to load the contents of a Microsoft Word document in plaintext and then access the original document's custom properties.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Hello world!")
doc.custom_document_properties.add("Location of writing", "123 Main St, London, UK")

doc.save(ARTIFACTS_DIR + "PlainTextDocument.custom_document_properties.docx")

plaintext = aw.PlainTextDocument(ARTIFACTS_DIR + "PlainTextDocument.custom_document_properties.docx")

self.assertEqual("Hello world!", plaintext.text.strip())
self.assertEqual("123 Main St, London, UK", plaintext.custom_document_properties.get_by_name("Location of writing").value)
```

### See Also

* module [aspose.words](../../)
* class [PlainTextDocument](../)

