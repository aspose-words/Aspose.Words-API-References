---
title: WriteProtection.IsWriteProtected
linktitle: IsWriteProtected
articleTitle: IsWriteProtected
second_title: Aspose.Words for .NET
description: Discover the WriteProtection IsWriteProtected property, easily check if a write protection password is active for enhanced security and data integrity.
type: docs
weight: 10
url: /net/aspose.words.settings/writeprotection/iswriteprotected/
---
## WriteProtection.IsWriteProtected property

Returns `true` when a write protection password is set.

```csharp
public bool IsWriteProtected { get; }
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
