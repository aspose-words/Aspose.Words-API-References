---
title: Document.protection_type property
linktitle: protection_type property
articleTitle: protection_type property
second_title: Aspose.Words for Python
description: "Document.protection_type property. Gets the currently active document protection type."
type: docs
weight: 340
url: /de/python-net/aspose.words/document/protection_type/
---

## Document.protection_type property

Gets the currently active document protection type.


```python
@property
def protection_type(self) -> aspose.words.ProtectionType:
    ...

```

### Remarks

This property allows to retrieve the currently set document protection type.
To change the document protection type use the [Document.protect()](../protect/#protectiontype_str)
and [Document.unprotect()](../unprotect/#default) methods.

When a document is protected, the user can make only limited changes,
such as adding annotations, making revisions, or completing a form.

Note that document protection is different from write protection.
Write protection is specified using the [Document.write_protection](../write_protection/)





### Examples

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

### See Also

* module [aspose.words](../../)
* class [Document](../)
* method [Document.protect()](../protect/#protectiontype_str)
* method [Document.unprotect()](../unprotect/#default)
* property [Document.write_protection](../write_protection/)

