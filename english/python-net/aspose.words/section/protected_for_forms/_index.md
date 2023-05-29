---
title: Section.protected_for_forms property
linktitle: protected_for_forms property
articleTitle: protected_for_forms property
second_title: Aspose.Words for Python
description: "Section.protected_for_forms property. True if the section is protected for forms"
type: docs
weight: 60
url: /python-net/aspose.words/section/protected_for_forms/
---

## Section.protected_for_forms property

True if the section is protected for forms. When a section is protected for forms,
users can select and modify text only in form fields in Microsoft Word.


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

* module [aspose.words](../../)
* class [Section](../)

