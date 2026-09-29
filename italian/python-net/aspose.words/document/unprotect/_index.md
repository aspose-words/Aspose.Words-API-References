---
title: Document.unprotect method
linktitle: unprotect method
articleTitle: unprotect method
second_title: Aspose.Words for Python
description: "aspose.words.Document.unprotect method"
type: docs
weight: 780
url: /it/python-net/aspose.words/document/unprotect/
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
# Se apriamo questo documento con Microsoft Word con l'intenzione di modificarlo,
# dovremo inserire la password per superare la protezione.
doc.save(file_name=ARTIFACTS_DIR + 'Document.Protect.docx')
# Nota che la protezione si applica solo agli utenti di Microsoft Word che aprono il nostro documento.
# Non abbiamo criptato il documento in alcun modo e non abbiamo bisogno della password per aprirlo e modificarlo programmaticamente.
protected_doc = aw.Document(file_name=ARTIFACTS_DIR + 'Document.Protect.docx')
self.assertEqual(aw.ProtectionType.READ_ONLY, protected_doc.protection_type)
builder = aw.DocumentBuilder(doc=protected_doc)
builder.writeln('Text added to a protected document.')
# Esistono due modi per rimuovere la protezione da un documento.
# 1 - Senza password:
doc.unprotect()
self.assertEqual(aw.ProtectionType.NO_PROTECTION, doc.protection_type)
doc.protect(type=aw.ProtectionType.READ_ONLY, password='NewPassword')
self.assertEqual(aw.ProtectionType.READ_ONLY, doc.protection_type)
doc.unprotect('WrongPassword')
self.assertEqual(aw.ProtectionType.READ_ONLY, doc.protection_type)
# 2 - Con la password corretta:
doc.unprotect('NewPassword')
self.assertEqual(aw.ProtectionType.NO_PROTECTION, doc.protection_type)
```

## See Also

* module [aspose.words](../../)
* class [Document](../)

