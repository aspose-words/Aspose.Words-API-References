---
title: BuiltInDocumentProperties.security property
linktitle: security property
articleTitle: security property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.security property. Specifies the security level of a document as a numeric value."
type: docs
weight: 250
url: /python-net/aspose.words.properties/builtindocumentproperties/security/
---

## BuiltInDocumentProperties.security property

Specifies the security level of a document as a numeric value.

Use this property for informational purposes only because Microsoft Word does not always
set this property. This property is available in DOC and OOXML documents only.

To protect or unprotect a document use the
[Document.protect()](../../../aspose.words/document/protect/#protectiontype_str) and [Document.unprotect()](../../../aspose.words/document/unprotect/#default) methods.

Aspose.Words updates this property to a correct value before saving a document.




### Examples

Shows how to use document properties to display the security level of a document.

```python
doc = aw.Document()

self.assertEqual(aw.properties.DocumentSecurity.NONE, doc.built_in_document_properties.security)

# If we configure a document to be read-only, it will display this status using the "security" built-in property.
doc.write_protection.read_only_recommended = True
doc.save(ARTIFACTS_DIR + "DocumentProperties.security.read_only_recommended.docx")

self.assertEqual(aw.properties.DocumentSecurity.READ_ONLY_RECOMMENDED,
    aw.Document(ARTIFACTS_DIR + "DocumentProperties.security.read_only_recommended.docx").built_in_document_properties.security)

# Write-protect a document, and then verify its security level.
doc = aw.Document()

self.assertFalse(doc.write_protection.is_write_protected)

doc.write_protection.set_password("MyPassword")

self.assertTrue(doc.write_protection.validate_password("MyPassword"))
self.assertTrue(doc.write_protection.is_write_protected)

doc.save(ARTIFACTS_DIR + "DocumentProperties.security.read_only_enforced.docx")

self.assertEqual(aw.properties.DocumentSecurity.READ_ONLY_ENFORCED,
    aw.Document(ARTIFACTS_DIR + "DocumentProperties.security.read_only_enforced.docx").built_in_document_properties.security)

# "security" is a descriptive property. We can edit its value manually.
doc = aw.Document()

doc.protect(aw.ProtectionType.ALLOW_ONLY_COMMENTS, "MyPassword")
doc.built_in_document_properties.security = aw.properties.DocumentSecurity.READ_ONLY_EXCEPT_ANNOTATIONS
doc.save(ARTIFACTS_DIR + "DocumentProperties.security.read_only_except_annotations.docx")

self.assertEqual(aw.properties.DocumentSecurity.READ_ONLY_EXCEPT_ANNOTATIONS,
    aw.Document(ARTIFACTS_DIR + "DocumentProperties.security.read_only_except_annotations.docx").built_in_document_properties.security)
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

