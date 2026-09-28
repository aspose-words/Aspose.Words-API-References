---
title: WriteProtection.read_only_recommended property
linktitle: read_only_recommended property
articleTitle: read_only_recommended property
second_title: Aspose.Words for Python
description: "WriteProtection.read_only_recommended property. Specifies whether the document author has recommended that the document be opened as read-only."
type: docs
weight: 20
url: /ar/python-net/aspose.words.settings/writeprotection/read_only_recommended/
---

## WriteProtection.read_only_recommended property

Specifies whether the document author has recommended that the document be opened as read-only.


```python
@property
def read_only_recommended(self) -> bool:
    ...

@read_only_recommended.setter
def read_only_recommended(self, value: bool):
    ...

```

### Examples

Shows how to protect a document with a password.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world! This document is protected.')
# أدخل كلمة مرور بطول يصل إلى 15 حرفًا، ثم تحقق من حالة حماية المستند.
doc.write_protection.set_password('MyPassword')
doc.write_protection.read_only_recommended = True
self.assertTrue(doc.write_protection.is_write_protected)
self.assertTrue(doc.write_protection.validate_password('MyPassword'))
# الحماية لا تمنع تحرير المستند برمجيًا، ولا تشفر المحتويات.
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

