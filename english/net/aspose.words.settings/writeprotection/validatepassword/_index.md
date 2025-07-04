---
title: WriteProtection.ValidatePassword
linktitle: ValidatePassword
articleTitle: ValidatePassword
second_title: Aspose.Words for .NET
description: Secure your documents with the WriteProtection ValidatePassword method. Easily verify if the password matches the document's protection for enhanced security.
type: docs
weight: 40
url: /net/aspose.words.settings/writeprotection/validatepassword/
---
## WriteProtection.ValidatePassword method

Returns `true` if the specified password is the same as the write-protection password the document was protected with. If document is not write-protected with password then returns `false`.

```csharp
public bool ValidatePassword(string password)
```

## Examples

Shows how to protect a document with a password.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This document is protected.");
// Enter a password up to 15 characters in length, and then verify the document's protection status.
doc.WriteProtection.SetPassword("MyPassword");
doc.WriteProtection.ReadOnlyRecommended = true;

Assert.That(doc.WriteProtection.IsWriteProtected, Is.True);
Assert.That(doc.WriteProtection.ValidatePassword("MyPassword"), Is.True);

// Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
doc.Save(ArtifactsDir + "Document.WriteProtection.docx");
doc = new Document(ArtifactsDir + "Document.WriteProtection.docx");

Assert.That(doc.WriteProtection.IsWriteProtected, Is.True);

builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln("Writing text in a protected document.");

Assert.That(doc.GetText().Trim(), Is.EqualTo("Hello world! This document is protected." +
                "\rWriting text in a protected document."));
```

### See Also

* class [WriteProtection](../)
* namespace [Aspose.Words.Settings](../../../aspose.words.settings/)
* assembly [Aspose.Words](../../../)
