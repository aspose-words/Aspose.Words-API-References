---
title: WriteProtection.is_write_protected property
linktitle: is_write_protected property
articleTitle: is_write_protected property
second_title: Aspose.Words for Python
description: "WriteProtection.is_write_protected property. Returns ``True`` when a write protection password is set."
type: docs
weight: 10
url: /python-net/aspose.words.settings/writeprotection/is_write_protected/
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
builder = aw.DocumentBuilder(doc)
builder.writeln("Hello world! This document is protected.")

# Enter a password up to 15 characters in length, and then verify the document's protection status.
doc.write_protection.set_password("MyPassword")
doc.write_protection.read_only_recommended = True

self.assertTrue(doc.write_protection.is_write_protected)
self.assertTrue(doc.write_protection.validate_password("MyPassword"))

# Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
doc.save(ARTIFACTS_DIR + "Document.write_protection.docx")
doc = aw.Document(ARTIFACTS_DIR + "Document.write_protection.docx")

self.assertTrue(doc.write_protection.is_write_protected)

builder = aw.DocumentBuilder(doc)
builder.move_to_document_end()
builder.writeln("Writing text in a protected document.")

self.assertEqual("Hello world! This document is protected." +
                "\rWriting text in a protected document.", doc.get_text().strip())
```

### See Also

* module [aspose.words.settings](../../)
* class [WriteProtection](../)

