---
title: BuiltInDocumentProperties.Security
linktitle: Security
articleTitle: Security
second_title: Aspose.Words for .NET
description: Discover the BuiltInDocumentProperties Security feature, defining your document's security level with precision. Enhance your document protection today!
type: docs
weight: 270
url: /net/aspose.words.properties/builtindocumentproperties/security/
---
## BuiltInDocumentProperties.Security property

Specifies the security level of a document as a numeric value.

```csharp
public DocumentSecurity Security { get; set; }
```

## Remarks

Use this property for informational purposes only because Microsoft Word does not always set this property. This property is available in DOC and OOXML documents only.

To protect or unprotect a document use the [`Protect`](../../../aspose.words/document/protect/) and [`Unprotect`](../../../aspose.words/document/unprotect/) methods.

Aspose.Words updates this property to a correct value before saving a document.

## Examples

Shows how to use document properties to display the security level of a document.

```csharp
Document doc = new Document();

Assert.That(doc.BuiltInDocumentProperties.Security, Is.EqualTo(DocumentSecurity.None));

// If we configure a document to be read-only, it will display this status using the "Security" built-in property.
doc.WriteProtection.ReadOnlyRecommended = true;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx");

Assert.That(new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx").BuiltInDocumentProperties.Security, Is.EqualTo(DocumentSecurity.ReadOnlyRecommended));

// Write-protect a document, and then verify its security level.
doc = new Document();

Assert.That(doc.WriteProtection.IsWriteProtected, Is.False);

doc.WriteProtection.SetPassword("MyPassword");

Assert.That(doc.WriteProtection.ValidatePassword("MyPassword"), Is.True);
Assert.That(doc.WriteProtection.IsWriteProtected, Is.True);

doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx");

Assert.That(new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx").BuiltInDocumentProperties.Security, Is.EqualTo(DocumentSecurity.ReadOnlyEnforced));

// "Security" is a descriptive property. We can edit its value manually.
doc = new Document();

doc.Protect(ProtectionType.AllowOnlyComments, "MyPassword");
doc.BuiltInDocumentProperties.Security = DocumentSecurity.ReadOnlyExceptAnnotations;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

Assert.That(new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx").BuiltInDocumentProperties.Security, Is.EqualTo(DocumentSecurity.ReadOnlyExceptAnnotations));
```

### See Also

* enum [DocumentSecurity](../../documentsecurity/)
* class [BuiltInDocumentProperties](../)
* namespace [Aspose.Words.Properties](../../../aspose.words.properties/)
* assembly [Aspose.Words](../../../)
