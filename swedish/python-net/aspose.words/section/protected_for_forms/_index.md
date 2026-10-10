---
title: Section.protected_for_forms property
linktitle: protected_for_forms property
articleTitle: protected_for_forms property
second_title: Aspose.Words for Python
description: "Section.protected_for_forms property. True if the section is protected for forms"
type: docs
weight: 60
url: /sv/python-net/aspose.words/section/protected_for_forms/
---

## Section.protected_for_forms property

True if the section is protected for forms. When a section is protected for forms,
users can select and modify text only in form fields in Microsoft Word.


```python
@property
def protected_for_forms(self) -> bool:
    ...

@protected_for_forms.setter
def protected_for_forms(self, value: bool):
    ...

```

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
# Applicera skrivskydd på varje avsnitt i dokumentet.
doc.protect(type=aw.ProtectionType.ALLOW_ONLY_FORM_FIELDS)
# Stäng av skrivskydd för det första avsnittet.
doc.sections[0].protected_for_forms = False
# I detta utdata-dokument kommer vi kunna redigera det första avsnittet fritt,
# och vi kommer bara kunna redigera innehållet i formulärfältet i det andra avsnittet.
doc.save(file_name=ARTIFACTS_DIR + 'Section.Protect.docx')
```

### See Also

* module [aspose.words](../../)
* class [Section](../)

