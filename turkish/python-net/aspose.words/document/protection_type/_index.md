---
title: Document.protection_type property
linktitle: protection_type property
articleTitle: protection_type property
second_title: Aspose.Words for Python
description: "Document.protection_type property. Gets the currently active document protection type."
type: docs
weight: 340
url: /tr/python-net/aspose.words/document/protection_type/
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
# Bu belgeyi düzenlemek amacıyla Microsoft Word ile açarsak,
# korumadan geçmek için şifreyi uygulamamız gerekir.
doc.save(file_name=ARTIFACTS_DIR + 'Document.Protect.docx')
# Korumanın yalnızca belgemizi açan Microsoft Word kullanıcılarına uygulandığını unutmayın.
# Belgeyi hiçbir şekilde şifrelemedik ve programlı olarak açmak ve düzenlemek için parolaya ihtiyacımız yok.
protected_doc = aw.Document(file_name=ARTIFACTS_DIR + 'Document.Protect.docx')
self.assertEqual(aw.ProtectionType.READ_ONLY, protected_doc.protection_type)
builder = aw.DocumentBuilder(doc=protected_doc)
builder.writeln('Text added to a protected document.')
# Bir belgeden korumayı kaldırmanın iki yolu vardır.
# 1 - Parola olmadan:
doc.unprotect()
self.assertEqual(aw.ProtectionType.NO_PROTECTION, doc.protection_type)
doc.protect(type=aw.ProtectionType.READ_ONLY, password='NewPassword')
self.assertEqual(aw.ProtectionType.READ_ONLY, doc.protection_type)
doc.unprotect('WrongPassword')
self.assertEqual(aw.ProtectionType.READ_ONLY, doc.protection_type)
# 2 - Doğru parola ile:
doc.unprotect('NewPassword')
self.assertEqual(aw.ProtectionType.NO_PROTECTION, doc.protection_type)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)
* method [Document.protect()](../protect/#protectiontype_str)
* method [Document.unprotect()](../unprotect/#default)
* property [Document.write_protection](../write_protection/)

