---
title: DocumentSecurity Enum
linktitle: DocumentSecurity
articleTitle: DocumentSecurity
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.DocumentSecurity enum to enhance your document's security. Easily specify and manage security levels for optimal protection.
type: docs
weight: 5220
url: /net/aspose.words.properties/documentsecurity/
---
## DocumentSecurity enumeration

Used as a value for the [`Security`](../builtindocumentproperties/security/) property. Specifies the security level of a document as a numeric value.

```csharp
[Flags]
public enum DocumentSecurity
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | There are no security states specified by the property. |
| PasswordProtected | `1` | The document is password protected. (Note has never been seen in a document so far). |
| ReadOnlyRecommended | `2` | The document to be opened read-only if possible, but the setting can be overridden. |
| ReadOnlyEnforced | `4` | The document to always be opened read-only. |
| ReadOnlyExceptAnnotations | `8` | The document to always be opened read-only except for annotations. |

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

* namespace [Aspose.Words.Properties](../../aspose.words.properties/)
* assembly [Aspose.Words](../../)
