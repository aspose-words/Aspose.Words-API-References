---
title: validate_password method
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns ``True`` if the specified password is the same as the write-protection password the document was protected with"
type: docs
weight: 40
url: /python-net/aspose.words.settings/writeprotection/validate_password/
---

## validate_password(password) {#str}

Returns ``True`` if the specified password is the same as the write-protection password the document was protected with.
If document is not write-protected with password then returns ``False``.



```python
def validate_password(self, password: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| password | str |  |

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

