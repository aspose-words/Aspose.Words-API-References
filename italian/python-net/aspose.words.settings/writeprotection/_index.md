---
title: WriteProtection class
linktitle: WriteProtection class
articleTitle: WriteProtection class
second_title: Aspose.Words for Python
description: "aspose.words.settings.WriteProtection class. Specifies write protection settings for a document"
type: docs
weight: 210
url: /it/python-net/aspose.words.settings/writeprotection/
---

## WriteProtection class

Specifies write protection settings for a document.
To learn more, visit the [Protect or Encrypt a Document](https://docs.aspose.com/words/python-net/protect-or-encrypt-a-document/) documentation article.




### Remarks

Write protection specifies whether the author has recommended that 
the document is to be opened as read-only and/or require a password to modify a document.

Write protection is different from document protection. Write protection is specified in 
Microsoft Word in the options of the Save As dialog box.

You do not create instances of this class directly. You access document protection settings
via the [Document.write_protection](../../aspose.words/document/write_protection/) property.




### Properties

| Name | Description |
| --- | --- |
| [is_write_protected](./is_write_protected/) | Returns ``True`` when a write protection password is set. |
| [read_only_recommended](./read_only_recommended/) | Specifies whether the document author has recommended that the document be opened as read-only. |

### Methods

| Name | Description |
| --- | --- |
|[ set_password(password)](./set_password/#str) | Sets the write protection password for the document. |
|[ validate_password(password)](./validate_password/#str) | Returns ``True`` if the specified password is the same as the write-protection password the document was protected with. If document is not write-protected with password then returns ``False``. |

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

* module [aspose.words.settings](../)

