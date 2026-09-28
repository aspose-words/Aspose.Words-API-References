---
title: WriteProtection.set_password method
linktitle: set_password method
articleTitle: set_password method
second_title: Aspose.Words for Python
description: "WriteProtection.set_password method. Sets the write protection password for the document."
type: docs
weight: 30
url: /fr/python-net/aspose.words.settings/writeprotection/set_password/
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
# Saisissez un mot de passe d'une longueur maximale de 15 caractères, puis vérifiez le statut de protection du document.
doc.write_protection.set_password('MyPassword')
doc.write_protection.read_only_recommended = True
self.assertTrue(doc.write_protection.is_write_protected)
self.assertTrue(doc.write_protection.validate_password('MyPassword'))
# La protection n'empêche pas le document d'être modifié par programme, et ne chiffre pas non plus le contenu.
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

