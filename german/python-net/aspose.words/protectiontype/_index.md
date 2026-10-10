---
title: ProtectionType enumeration
linktitle: ProtectionType enumeration
articleTitle: ProtectionType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.ProtectionType enumeration. Protection type for a document."
type: docs
weight: 1020
url: /de/python-net/aspose.words/protectiontype/
---

## ProtectionType enumeration

Protection type for a document.


### Members

| Name | Description |
| --- | --- |
| ALLOW_ONLY_COMMENTS | User can only modify comments in the document. |
| ALLOW_ONLY_FORM_FIELDS | User can only enter data in the form fields in the document. |
| ALLOW_ONLY_REVISIONS | User can only add revision marks to the document. |
| READ_ONLY | No changes are allowed to the document. Available since Microsoft Word 2003. |
| NO_PROTECTION | The document is not protected. |

### Examples

Shows how to turn off protection for a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Section 1. Hello world!')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.writeln('Section 2. Hello again!')
builder.write('Please enter text here: ')
builder.insert_text_input('TextInput1', aw.fields.TextFormFieldType.REGULAR, '', 'Placeholder text', 0)
# Schreibschutz auf jeden Abschnitt im Dokument anwenden.
doc.protect(type=aw.ProtectionType.ALLOW_ONLY_FORM_FIELDS)
# Schreibschutz für den ersten Abschnitt deaktivieren.
doc.sections[0].protected_for_forms = False
# In diesem Ausgabedokument können wir den ersten Abschnitt frei bearbeiten,
# und wir können nur den Inhalt des Formularfelds im zweiten Abschnitt bearbeiten.
doc.save(file_name=ARTIFACTS_DIR + 'Section.Protect.docx')
```

### See Also

* module [aspose.words](../)

