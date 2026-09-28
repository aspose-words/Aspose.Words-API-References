---
title: DocumentSecurity enumeration
linktitle: DocumentSecurity enumeration
articleTitle: DocumentSecurity enumeration
second_title: Aspose.Words for Python
description: "aspose.words.properties.DocumentSecurity enumeration. Used as a value for the [BuiltInDocumentProperties.security](../builtindocumentproperties/security/) property"
type: docs
weight: 50
url: /zh/python-net/aspose.words.properties/documentsecurity/
---

## DocumentSecurity enumeration

Used as a value for the [BuiltInDocumentProperties.security](../builtindocumentproperties/security/) property.
Specifies the security level of a document as a numeric value.



### Members

| Name | Description |
| --- | --- |
| NONE | There are no security states specified by the property. |
| PASSWORD_PROTECTED | The document is password protected. (Note has never been seen in a document so far). |
| READ_ONLY_RECOMMENDED | The document to be opened read-only if possible, but the setting can be overridden. |
| READ_ONLY_ENFORCED | The document to always be opened read-only. |
| READ_ONLY_EXCEPT_ANNOTATIONS | The document to always be opened read-only except for annotations. |

### Examples

Shows how to use document properties to display the security level of a document.

```python
doc = aw.Document()
self.assertEqual(aw.properties.DocumentSecurity.NONE, doc.built_in_document_properties.security)
# 如果我们将文档配置为只读，它将使用 “Security” 内置属性显示此状态。
doc.write_protection.read_only_recommended = True
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.Security.ReadOnlyRecommended.docx')
self.assertEqual(aw.properties.DocumentSecurity.READ_ONLY_RECOMMENDED, aw.Document(file_name=ARTIFACTS_DIR + 'DocumentProperties.Security.ReadOnlyRecommended.docx').built_in_document_properties.security)
# 对文档进行写保护，然后验证其安全级别。
doc = aw.Document()
self.assertFalse(doc.write_protection.is_write_protected)
doc.write_protection.set_password('MyPassword')
self.assertTrue(doc.write_protection.validate_password('MyPassword'))
self.assertTrue(doc.write_protection.is_write_protected)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.Security.ReadOnlyEnforced.docx')
self.assertEqual(aw.properties.DocumentSecurity.READ_ONLY_ENFORCED, aw.Document(file_name=ARTIFACTS_DIR + 'DocumentProperties.Security.ReadOnlyEnforced.docx').built_in_document_properties.security)
# “Security” 是描述性属性。我们可以手动编辑其值。
doc = aw.Document()
doc.protect(type=aw.ProtectionType.ALLOW_ONLY_COMMENTS, password='MyPassword')
doc.built_in_document_properties.security = aw.properties.DocumentSecurity.READ_ONLY_EXCEPT_ANNOTATIONS
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.Security.ReadOnlyExceptAnnotations.docx')
self.assertEqual(aw.properties.DocumentSecurity.READ_ONLY_EXCEPT_ANNOTATIONS, aw.Document(file_name=ARTIFACTS_DIR + 'DocumentProperties.Security.ReadOnlyExceptAnnotations.docx').built_in_document_properties.security)
```

### See Also

* module [aspose.words.properties](../)

