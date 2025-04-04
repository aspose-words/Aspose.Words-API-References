---
title: DocumentSecurity enumeration
linktitle: DocumentSecurity enumeration
articleTitle: DocumentSecurity enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Properties.DocumentSecurity enumeration. Used as a value for the [BuiltInDocumentProperties.security](../builtindocumentproperties/security/) property"
type: docs
weight: 50
url: /nodejs-net/aspose.words.properties/documentsecurity/
---

## DocumentSecurity enumeration

Used as a value for the [BuiltInDocumentProperties.security](../builtindocumentproperties/security/) property.
Specifies the security level of a document as a numeric value.



### Members

| Name | Description |
| --- | --- |
| None | There are no security states specified by the property. |
| PasswordProtected | The document is password protected. (Note has never been seen in a document so far). |
| ReadOnlyRecommended | The document to be opened read-only if possible, but the setting can be overridden. |
| ReadOnlyEnforced | The document to always be opened read-only. |
| ReadOnlyExceptAnnotations | The document to always be opened read-only except for annotations. |

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

* module [Aspose.Words.Properties](../)

