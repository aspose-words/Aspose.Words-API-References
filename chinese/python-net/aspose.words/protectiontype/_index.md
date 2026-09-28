---
title: ProtectionType enumeration
linktitle: ProtectionType enumeration
articleTitle: ProtectionType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.ProtectionType enumeration. Protection type for a document."
type: docs
weight: 1020
url: /zh/python-net/aspose.words/protectiontype/
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
# 对文档中的每个章节应用写保护。
doc.protect(type=aw.ProtectionType.ALLOW_ONLY_FORM_FIELDS)
# 关闭第一章节的写保护。
doc.sections[0].protected_for_forms = False
# 在此输出文档中，我们可以自由编辑第一章节，
# 并且只能编辑第二章节中表单字段的内容。
doc.save(file_name=ARTIFACTS_DIR + 'Section.Protect.docx')
```

### See Also

* module [aspose.words](../)

