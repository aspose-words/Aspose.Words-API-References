---
title: Document.protection_type property
linktitle: protection_type property
articleTitle: protection_type property
second_title: Aspose.Words for Python
description: "Document.protection_type property. Gets the currently active document protection type."
type: docs
weight: 340
url: /zh/python-net/aspose.words/document/protection_type/
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

### See Also

* module [aspose.words](../../)
* class [Document](../)
* method [Document.protect()](../protect/#protectiontype_str)
* method [Document.unprotect()](../unprotect/#default)
* property [Document.write_protection](../write_protection/)

