---
title: protect method
second_title: Aspose.Words for Python via .NET API Reference
description: "aspose.words.Document.protect method"
type: docs
weight: 620
url: /python-net/aspose.words/document/protect/
---

## protect(type) {#protectiontype}

Protects the document from changes without changing the existing password or assigns a random password.


```python
def protect(self, type: aspose.words.ProtectionType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| type | [ProtectionType](../../protectiontype/) |  |

When a document is protected, the user can make only limited changes,
such as adding annotations, making revisions, or completing a form.

When you protect a document, and the document already has a protection password,
the existing protection password is not changed.

When you protect a document, and the document does not have a protection password,
this method assigns a random password that makes it impossible to unprotect the document
in Microsoft Word, but you still can unprotect the document in Aspose.Words as it does not
require a password when unprotecting.




## protect(type, password) {#protectiontype_str}

Protects the document from changes and optionally sets a protection password.


```python
def protect(self, type: aspose.words.ProtectionType, password: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| type | [ProtectionType](../../protectiontype/) |  |
| password | str |  |

When a document is protected, the user can make only limited changes,
such as adding annotations, making revisions, or completing a form.

Note that document protection is different from write protection.
Write protection is specified using the [Document.write_protection](../write_protection/).




## Examples

Shows how to turn off protection for a section.

```python
doc = aw.Document()

builder = aw.DocumentBuilder(doc)
builder.writeln("Section 1. Hello world!")
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)

builder.writeln("Section 2. Hello again!")
builder.write("Please enter text here: ")
builder.insert_text_input("TextInput1", aw.fields.TextFormFieldType.REGULAR, "", "Placeholder text", 0)

# Apply write protection to every section in the document.
doc.protect(aw.ProtectionType.ALLOW_ONLY_FORM_FIELDS)

# Turn off write protection for the first section.
doc.sections[0].protected_for_forms = False

# In this output document, we will be able to edit the first section freely,
# and we will only be able to edit the contents of the form field in the second section.
doc.save(ARTIFACTS_DIR + "Section.protect.docx")
```

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

