---
title: Document.protect method
linktitle: protect method
articleTitle: protect method
second_title: Aspose.Words for Python
description: "aspose.words.Document.protect method"
type: docs
weight: 690
url: /zh/python-net/aspose.words/document/protect/
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
# 对文档中的每个章节应用写保护。
doc.protect(type=aw.ProtectionType.ALLOW_ONLY_FORM_FIELDS)
# 关闭第一章节的写保护。
doc.sections[0].protected_for_forms = False
# 在此输出文档中，我们可以自由编辑第一章节，
# 并且只能编辑第二章节中表单字段的内容。
doc.save(file_name=ARTIFACTS_DIR + 'Section.Protect.docx')
```

Shows how to protect and unprotect a document.

```python
doc = aw.Document()
doc.protect(type=aw.ProtectionType.READ_ONLY, password='password')
self.assertEqual(aw.ProtectionType.READ_ONLY, doc.protection_type)
# 如果我们使用 Microsoft Word 打开此文档并打算编辑它，
# 我们需要输入密码才能通过保护。
doc.save(file_name=ARTIFACTS_DIR + 'Document.Protect.docx')
# 请注意，保护仅适用于使用 Microsoft Word 打开我们文档的用户。
# 我们没有以任何方式加密文档，也不需要密码即可以编程方式打开和编辑它。
protected_doc = aw.Document(file_name=ARTIFACTS_DIR + 'Document.Protect.docx')
self.assertEqual(aw.ProtectionType.READ_ONLY, protected_doc.protection_type)
builder = aw.DocumentBuilder(doc=protected_doc)
builder.writeln('Text added to a protected document.')
# 有两种方法可以移除文档的保护。
# 1 - 不使用密码：
doc.unprotect()
self.assertEqual(aw.ProtectionType.NO_PROTECTION, doc.protection_type)
doc.protect(type=aw.ProtectionType.READ_ONLY, password='NewPassword')
self.assertEqual(aw.ProtectionType.READ_ONLY, doc.protection_type)
doc.unprotect('WrongPassword')
self.assertEqual(aw.ProtectionType.READ_ONLY, doc.protection_type)
# 2 - 使用正确的密码：
doc.unprotect('NewPassword')
self.assertEqual(aw.ProtectionType.NO_PROTECTION, doc.protection_type)
```

## See Also

* module [aspose.words](../../)
* class [Document](../)

