---
title: Document.unprotect method
linktitle: unprotect method
articleTitle: unprotect method
second_title: Aspose.Words for Python
description: "aspose.words.Document.unprotect method"
type: docs
weight: 780
url: /zh/python-net/aspose.words/document/unprotect/
---

## unprotect() {#default}

Removes protection from the document regardless of the password.


```python
def unprotect(self):
    ...
```

### Remarks

This method unprotects the document even if it has a protection password.

Note that document protection is different from write protection.
Write protection is specified using the [Document.write_protection](../write_protection/).




## unprotect(password) {#str}

Removes protection from the document if a correct password is specified.


```python
def unprotect(self, password: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| password | str | The password to unprotect the document with. |

### Remarks

This method unprotects the document only if a correct password is specified.

Note that document protection is different from write protection.
Write protection is specified using the [Document.write_protection](../write_protection/).




### Returns

``True`` if a correct password was specified and the document was unprotected.


## Examples

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

