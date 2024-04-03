---
title: Document.unprotect method
linktitle: unprotect method
articleTitle: unprotect method
second_title: Aspose.Words for Python
description: "aspose.words.Document.unprotect method"
type: docs
weight: 750
url: /python-net/aspose.words/document/unprotect/
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
doc.protect(aw.ProtectionType.READ_ONLY, "password")

self.assertEqual(aw.ProtectionType.READ_ONLY, doc.protection_type)

# If we open this document with Microsoft Word intending to edit it,
# we will need to apply the password to get through the protection.
doc.save(ARTIFACTS_DIR + "Document.protect_unprotect.docx")

# Note that the protection only applies to Microsoft Word users opening our document.
# We have not encrypted the document in any way, and we do not need the password to open and edit it programmatically.
protected_doc = aw.Document(ARTIFACTS_DIR + "Document.protect_unprotect.docx")

self.assertEqual(aw.ProtectionType.READ_ONLY, protected_doc.protection_type)

builder = aw.DocumentBuilder(protected_doc)
builder.writeln("Text added to a protected document.")

# There are two ways of removing protection from a document.
# 1 - With no password:
doc.unprotect()

self.assertEqual(aw.ProtectionType.NO_PROTECTION, doc.protection_type)

doc.protect(aw.ProtectionType.READ_ONLY, "NewPassword")

self.assertEqual(aw.ProtectionType.READ_ONLY, doc.protection_type)

doc.unprotect("WrongPassword")

self.assertEqual(aw.ProtectionType.READ_ONLY, doc.protection_type)

# 2 - With the correct password:
doc.unprotect("NewPassword")

self.assertEqual(aw.ProtectionType.NO_PROTECTION, doc.protection_type)
```

## See Also

* module [aspose.words](../../)
* class [Document](../)

