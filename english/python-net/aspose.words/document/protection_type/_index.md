---
title: Document.protection_type property
linktitle: protection_type property
articleTitle: protection_type property
second_title: Aspose.Words for Python
description: "Document.protection_type property. Gets the currently active document protection type."
type: docs
weight: 340
url: /python-net/aspose.words/document/protection_type/
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

### See Also

* module [aspose.words](../../)
* class [Document](../)
* method [Document.protect()](../protect/#protectiontype_str)
* method [Document.unprotect()](../unprotect/#default)
* property [Document.write_protection](../write_protection/)

