---
title: BuiltInDocumentProperties.security property
linktitle: security property
articleTitle: security property
second_title: Aspose.Words for NodeJs
description: "BuiltInDocumentProperties.security property. Specifies the security level of a document as a numeric value."
type: docs
weight: 250
url: /nodejs-net/Aspose.Words.Properties/builtindocumentproperties/security/
---

## BuiltInDocumentProperties.security property

Specifies the security level of a document as a numeric value.


```js
get security(): Aspose.Words.Properties.DocumentSecurity
```

### Remarks

Use this property for informational purposes only because Microsoft Word does not always
set this property. This property is available in DOC and OOXML documents only.

To protect or unprotect a document use the
[Document.protect()](../../../aspose.words/document/protect/#protectiontype_string) and [Document.unprotect()](../../../aspose.words/document/unprotect/#default) methods.

Aspose.Words updates this property to a correct value before saving a document.




### Examples

Shows how to use document properties to display the security level of a document.

```js
let doc = new aw.Document();

expect(doc.builtInDocumentProperties.security).toEqual(aw.Properties.DocumentSecurity.None);

// If we configure a document to be read-only, it will display this status using the "Security" built-in property.
doc.writeProtection.readOnlyRecommended = true;
doc.save(base.artifactsDir + "DocumentProperties.security.readOnlyRecommended.docx");

expect(new aw.Document(base.artifactsDir + "DocumentProperties.security.readOnlyRecommended.docx")
  .builtInDocumentProperties.security).toEqual(aw.Properties.DocumentSecurity.ReadOnlyRecommended);

// Write-protect a document, and then verify its security level.
doc = new aw.Document();

expect(doc.writeProtection.isWriteProtected).toEqual(false);

doc.writeProtection.setPassword("MyPassword");

expect(doc.writeProtection.validatePassword("MyPassword")).toEqual(true);
expect(doc.writeProtection.isWriteProtected).toEqual(true);

doc.save(base.artifactsDir + "DocumentProperties.security.readOnlyEnforced.docx");

expect(new aw.Document(base.artifactsDir + "DocumentProperties.security.readOnlyEnforced.docx")
  .builtInDocumentProperties.security).toEqual(aw.Properties.DocumentSecurity.ReadOnlyEnforced);

// "Security" is a descriptive property. We can edit its value manually.
doc = new aw.Document();

doc.protect(aw.ProtectionType.AllowOnlyComments, "MyPassword");
doc.builtInDocumentProperties.security = aw.Properties.DocumentSecurity.ReadOnlyExceptAnnotations;
doc.save(base.artifactsDir + "DocumentProperties.security.readOnlyExceptAnnotations.docx");

expect(new aw.Document(base.artifactsDir + "DocumentProperties.security.readOnlyExceptAnnotations.docx")
  .builtInDocumentProperties.security).toEqual(aw.Properties.DocumentSecurity.ReadOnlyExceptAnnotations);
```

### See Also

* module [Aspose.Words.Properties](../../)
* class [BuiltInDocumentProperties](../)

