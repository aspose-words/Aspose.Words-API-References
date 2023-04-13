---
title: Document.Unprotect
linktitle: Unprotect
second_title: Aspose.Words for .NET API Reference
description: Document method. Removes protection from the document regardless of the password in C#.
type: docs
weight: 740
url: /net/aspose.words/document/unprotect/
---
## Unprotect() {#unprotect_1}

Removes protection from the document regardless of the password.

```csharp
public void Unprotect()
```

## Remarks

This method unprotects the document even if it has a protection password.

Note that document protection is different from write protection. Write protection is specified using the [`WriteProtection`](../writeprotection/).

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

* class [Document](../)
* namespace [Aspose.Words](../../document/)
* assembly [Aspose.Words](../../../)

---

## Unprotect(*string*) {#unprotect}

Removes protection from the document if a correct password is specified.

```csharp
public bool Unprotect(string password)
```

| Parameter | Type | Description |
| --- | --- | --- |
| password | String | The password to unprotect the document with. |

### Return Value

`true` if a correct password was specified and the document was unprotected.

## Remarks

This method unprotects the document only if a correct password is specified.

Note that document protection is different from write protection. Write protection is specified using the [`WriteProtection`](../writeprotection/).

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

* class [Document](../)
* namespace [Aspose.Words](../../document/)
* assembly [Aspose.Words](../../../)
