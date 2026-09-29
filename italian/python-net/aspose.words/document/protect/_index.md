---
title: Document.protect method
linktitle: protect method
articleTitle: protect method
second_title: Aspose.Words for Python
description: "aspose.words.Document.protect method"
type: docs
weight: 690
url: /it/python-net/aspose.words/document/protect/
---

## protect(type) {#protectiontype}

Protects the document from changes without changing the existing password or assigns a random password.


```python
def protect(self, type: aspose.words.ProtectionType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| type | [ProtectionType](../../protectiontype/) | Specifies the protection type for the document. |

### Remarks

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
| type | [ProtectionType](../../protectiontype/) | Specifies the protection type for the document. |
| password | str | The password to protect the document with. Specify ``None`` or empty string if you want to protect the document without a password. |

### Remarks

When a document is protected, the user can make only limited changes,
such as adding annotations, making revisions, or completing a form.

Note that document protection is different from write protection.
Write protection is specified using the [Document.write_protection](../write_protection/).




## Examples

Shows how to turn off protection for a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Section 1. Hello world!')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.writeln('Section 2. Hello again!')
builder.write('Please enter text here: ')
builder.insert_text_input('TextInput1', aw.fields.TextFormFieldType.REGULAR, '', 'Placeholder text', 0)
# Applicare la protezione di scrittura a ogni sezione del documento.
doc.protect(type=aw.ProtectionType.ALLOW_ONLY_FORM_FIELDS)
# Disattivare la protezione di scrittura per la prima sezione.
doc.sections[0].protected_for_forms = False
# In questo documento di output, potremo modificare liberamente la prima sezione,
# e potremo modificare solo il contenuto del campo modulo nella seconda sezione.
doc.save(file_name=ARTIFACTS_DIR + 'Section.Protect.docx')
```

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

