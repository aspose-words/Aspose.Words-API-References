---
title: Document.unprotect method
linktitle: unprotect method
articleTitle: unprotect method
second_title: Aspose.Words for Python
description: "aspose.words.Document.unprotect method"
type: docs
weight: 780
url: /de/python-net/aspose.words/document/unprotect/
---

## unprotect() {#default}

Removes protection from the document regardless of the password.


```python
def unprotect(self):
    ...
```

### Remarks

This method unprotects the document even if it has a protection password.

Note that document protection is different from write protection.
Write protection is specified using the [Document.write_protection](../write_protection/).




## unprotect(password) {#str}

Removes protection from the document if a correct password is specified.


```python
def unprotect(self, password: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| password | str | The password to unprotect the document with. |

### Remarks

This method unprotects the document only if a correct password is specified.

Note that document protection is different from write protection.
Write protection is specified using the [Document.write_protection](../write_protection/).




### Returns

``True`` if a correct password was specified and the document was unprotected.


## Examples

Shows how to protect and unprotect a document.

```python
doc = aw.Document()
doc.protect(type=aw.ProtectionType.READ_ONLY, password='password')
self.assertEqual(aw.ProtectionType.READ_ONLY, doc.protection_type)
# Wenn wir dieses Dokument mit Microsoft Word öffnen, um es zu bearbeiten,
# müssen wir das Passwort eingeben, um die Schutzfunktion zu umgehen.
doc.save(file_name=ARTIFACTS_DIR + 'Document.Protect.docx')
# Beachten Sie, dass der Schutz nur für Microsoft Word‑Benutzer gilt, die unser Dokument öffnen.
# Wir haben das Dokument in keiner Weise verschlüsselt und benötigen das Passwort nicht, um es programmgesteuert zu öffnen und zu bearbeiten.
protected_doc = aw.Document(file_name=ARTIFACTS_DIR + 'Document.Protect.docx')
self.assertEqual(aw.ProtectionType.READ_ONLY, protected_doc.protection_type)
builder = aw.DocumentBuilder(doc=protected_doc)
builder.writeln('Text added to a protected document.')
# Es gibt zwei Möglichkeiten, den Schutz eines Dokuments zu entfernen.
# 1 - Ohne Passwort:
doc.unprotect()
self.assertEqual(aw.ProtectionType.NO_PROTECTION, doc.protection_type)
doc.protect(type=aw.ProtectionType.READ_ONLY, password='NewPassword')
self.assertEqual(aw.ProtectionType.READ_ONLY, doc.protection_type)
doc.unprotect('WrongPassword')
self.assertEqual(aw.ProtectionType.READ_ONLY, doc.protection_type)
# 2 - Mit dem richtigen Passwort:
doc.unprotect('NewPassword')
self.assertEqual(aw.ProtectionType.NO_PROTECTION, doc.protection_type)
```

## See Also

* module [aspose.words](../../)
* class [Document](../)

