---
title: ProtectionType enumeration
second_title: Aspose.Words for Python via .NET API Reference
description: "Protection type for a document."
type: docs
weight: 890
url: /python-net/aspose.words/protectiontype/
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

### See Also

* module [aspose.words](../)

