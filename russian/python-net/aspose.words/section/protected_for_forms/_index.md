---
title: Section.protected_for_forms property
linktitle: protected_for_forms property
articleTitle: protected_for_forms property
second_title: Aspose.Words for Python
description: "Section.protected_for_forms property. True if the section is protected for forms"
type: docs
weight: 60
url: /ru/python-net/aspose.words/section/protected_for_forms/
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
# Примените защиту от записи ко всем разделам в документе.
doc.protect(type=aw.ProtectionType.ALLOW_ONLY_FORM_FIELDS)
# Отключите защиту от записи для первого раздела.
doc.sections[0].protected_for_forms = False
# В этом выходном документе мы сможем свободно редактировать первый раздел,
# и сможем редактировать только содержимое поля формы во втором разделе.
doc.save(file_name=ARTIFACTS_DIR + 'Section.Protect.docx')
```

### See Also

* module [aspose.words](../../)
* class [Section](../)

