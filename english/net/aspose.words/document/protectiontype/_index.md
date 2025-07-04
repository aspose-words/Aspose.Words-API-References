---
title: Document.ProtectionType
linktitle: ProtectionType
articleTitle: ProtectionType
second_title: Aspose.Words for .NET
description: Discover the active document protection type for enhanced security and data integrity. Safeguard your files effortlessly with our advanced features.
type: docs
weight: 340
url: /net/aspose.words/document/protectiontype/
---
## Document.ProtectionType property

Gets the currently active document protection type.

```csharp
public ProtectionType ProtectionType { get; }
```

## Remarks

This property allows to retrieve the currently set document protection type. To change the document protection type use the [`Protect`](../protect/) and [`Unprotect`](../unprotect/) methods.

When a document is protected, the user can make only limited changes, such as adding annotations, making revisions, or completing a form.

Note that document protection is different from write protection. Write protection is specified using the [`WriteProtection`](../writeprotection/)

## Examples

Shows how to protect and unprotect a document.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.That(doc.ProtectionType, Is.EqualTo(ProtectionType.ReadOnly));

// If we open this document with Microsoft Word intending to edit it,
// we will need to apply the password to get through the protection.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// Note that the protection only applies to Microsoft Word users opening our document.
// We have not encrypted the document in any way, and we do not need the password to open and edit it programmatically.
Document protectedDoc = new Document(ArtifactsDir + "Document.Protect.docx");

Assert.That(protectedDoc.ProtectionType, Is.EqualTo(ProtectionType.ReadOnly));

DocumentBuilder builder = new DocumentBuilder(protectedDoc);
builder.Writeln("Text added to a protected document.");
// There are two ways of removing protection from a document.
// 1 - With no password:
doc.Unprotect();

Assert.That(doc.ProtectionType, Is.EqualTo(ProtectionType.NoProtection));

doc.Protect(ProtectionType.ReadOnly, "NewPassword");

Assert.That(doc.ProtectionType, Is.EqualTo(ProtectionType.ReadOnly));

doc.Unprotect("WrongPassword");

Assert.That(doc.ProtectionType, Is.EqualTo(ProtectionType.ReadOnly));

// 2 - With the correct password:
doc.Unprotect("NewPassword");

Assert.That(doc.ProtectionType, Is.EqualTo(ProtectionType.NoProtection));
```

### See Also

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
