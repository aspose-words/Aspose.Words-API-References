---
title: Document.write_protection property
linktitle: write_protection property
articleTitle: write_protection property
second_title: Aspose.Words for Python
description: "Document.write_protection property. Provides access to the document write protection options."
type: docs
weight: 530
url: /it/python-net/aspose.words/document/write_protection/
---

## Document.write_protection property

Provides access to the document write protection options.


```python
@property
def write_protection(self) -> aspose.words.settings.WriteProtection:
    ...

```

### Examples

Shows how to protect a document with a password.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world! This document is protected.')
# Inserisci una password lunga fino a 15 caratteri, quindi verifica lo stato di protezione del documento.
doc.write_protection.set_password('MyPassword')
doc.write_protection.read_only_recommended = True
self.assertTrue(doc.write_protection.is_write_protected)
self.assertTrue(doc.write_protection.validate_password('MyPassword'))
# La protezione non impedisce al documento di essere modificato programmaticamente, né cifra il contenuto.
doc.save(file_name=ARTIFACTS_DIR + 'Document.WriteProtection.docx')
doc = aw.Document(file_name=ARTIFACTS_DIR + 'Document.WriteProtection.docx')
self.assertTrue(doc.write_protection.is_write_protected)
builder = aw.DocumentBuilder(doc=doc)
builder.move_to_document_end()
builder.writeln('Writing text in a protected document.')
self.assertEqual('Hello world! This document is protected.' + '\rWriting text in a protected document.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

