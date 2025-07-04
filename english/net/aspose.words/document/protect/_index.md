---
title: Document.Protect
linktitle: Protect
articleTitle: Protect
second_title: Aspose.Words for .NET
description: Secure your documents effortlessly with Document Protect. Prevent unauthorized changes while keeping your existing password intact or using a random one.
type: docs
weight: 690
url: /net/aspose.words/document/protect/
---
## Protect(*[ProtectionType](../../protectiontype/)*) {#protect}

Protects the document from changes without changing the existing password or assigns a random password.

```csharp
public void Protect(ProtectionType type)
```

| Parameter | Type | Description |
| --- | --- | --- |
| type | ProtectionType | Specifies the protection type for the document. |

## Remarks

When a document is protected, the user can make only limited changes, such as adding annotations, making revisions, or completing a form.

When you protect a document, and the document already has a protection password, the existing protection password is not changed.

When you protect a document, and the document does not have a protection password, this method assigns a random password that makes it impossible to unprotect the document in Microsoft Word, but you still can unprotect the document in Aspose.Words as it does not require a password when unprotecting.

## Examples

Shows how to turn off protection for a section.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Section 1. Hello world!");
builder.InsertBreak(BreakType.SectionBreakNewPage);

builder.Writeln("Section 2. Hello again!");
builder.Write("Please enter text here: ");
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Apply write protection to every section in the document.
doc.Protect(ProtectionType.AllowOnlyFormFields);

// Turn off write protection for the first section.
doc.Sections[0].ProtectedForForms = false;

// In this output document, we will be able to edit the first section freely,
// and we will only be able to edit the contents of the form field in the second section.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### See Also

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## Protect(*[ProtectionType](../../protectiontype/), string*) {#protect_1}

Protects the document from changes and optionally sets a protection password.

```csharp
public void Protect(ProtectionType type, string password)
```

| Parameter | Type | Description |
| --- | --- | --- |
| type | ProtectionType | Specifies the protection type for the document. |
| password | String | The password to protect the document with. Specify `null` or empty string if you want to protect the document without a password. |

## Remarks

When a document is protected, the user can make only limited changes, such as adding annotations, making revisions, or completing a form.

Note that document protection is different from write protection. Write protection is specified using the [`WriteProtection`](../writeprotection/).

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
