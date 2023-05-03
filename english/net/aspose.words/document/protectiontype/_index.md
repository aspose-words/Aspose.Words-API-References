---
title: Document.ProtectionType
linktitle: ProtectionType
second_title: Aspose.Words for .NET API Reference
description: Document ProtectionType property. Gets the currently active document protection type in C#.
type: docs
weight: 330
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

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// If we open this document with Microsoft Word intending to edit it,
// we will need to apply the password to get through the protection.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// Note that the protection only applies to Microsoft Word users opening our document.
// We have not encrypted the document in any way, and we do not need the password to open and edit it programmatically.
Document protectedDoc = new Document(ArtifactsDir + "Document.Protect.docx");

Assert.AreEqual(ProtectionType.ReadOnly, protectedDoc.ProtectionType);

DocumentBuilder builder = new DocumentBuilder(protectedDoc);
builder.Writeln("Text added to a protected document.");
// There are two ways of removing protection from a document.
// 1 - With no password:
doc.Unprotect();

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);

doc.Protect(ProtectionType.ReadOnly, "NewPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

doc.Unprotect("WrongPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// 2 - With the correct password:
doc.Unprotect("NewPassword");

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);
```

### See Also

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* namespace [Aspose.Words](../../document/)
* assembly [Aspose.Words](../../../)
