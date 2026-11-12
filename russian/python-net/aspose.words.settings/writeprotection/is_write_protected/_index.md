---
title: WriteProtection.is_write_protected property
linktitle: is_write_protected property
articleTitle: is_write_protected property
second_title: Aspose.Words for Python
description: "WriteProtection.is_write_protected property. Returns ``True`` when a write protection password is set."
type: docs
weight: 10
url: /ru/python-net/aspose.words.settings/writeprotection/is_write_protected/
---

## WriteProtection.is_write_protected property

Returns ``True`` when a write protection password is set.



```python
@property
def is_write_protected(self) -> bool:
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

* module [aspose.words.settings](../../)
* class [WriteProtection](../)

