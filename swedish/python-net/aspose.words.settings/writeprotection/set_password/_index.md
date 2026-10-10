---
title: WriteProtection.set_password method
linktitle: set_password method
articleTitle: set_password method
second_title: Aspose.Words for Python
description: "WriteProtection.set_password method. Sets the write protection password for the document."
type: docs
weight: 30
url: /sv/python-net/aspose.words.settings/writeprotection/set_password/
---

## set_password(password) {#str}

Sets the write protection password for the document.


```python
def set_password(self, password: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| password | str | The password to set. Cannot be ``None``, but can be an empty string. |

### Remarks

If a password is set, Microsoft Word will require the user to enter it or open 
the document as read-only.




### Examples

Shows how to protect a document with a password.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world! This document is protected.')
# Ange ett lösenord på upp till 15 tecken och verifiera sedan dokumentets skyddstatus.
doc.write_protection.set_password('MyPassword')
doc.write_protection.read_only_recommended = True
self.assertTrue(doc.write_protection.is_write_protected)
self.assertTrue(doc.write_protection.validate_password('MyPassword'))
# Skydd hindrar inte dokumentet från att redigeras programmässigt, och det krypterar inte heller innehållet.
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

