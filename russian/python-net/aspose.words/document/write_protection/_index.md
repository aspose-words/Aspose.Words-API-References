---
title: Document.write_protection property
linktitle: write_protection property
articleTitle: write_protection property
second_title: Aspose.Words for Python
description: "Document.write_protection property. Provides access to the document write protection options."
type: docs
weight: 530
url: /ru/python-net/aspose.words/document/write_protection/
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
# Введите пароль длиной до 15 символов, а затем проверьте статус защиты документа.
doc.write_protection.set_password('MyPassword')
doc.write_protection.read_only_recommended = True
self.assertTrue(doc.write_protection.is_write_protected)
self.assertTrue(doc.write_protection.validate_password('MyPassword'))
# Защита не препятствует программному редактированию документа и не шифрует его содержимое.
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

