---
title: ReadOnlyRecommended
second_title: Aspose.Words for .NET API Reference
description: WriteProtection property. Specifies whether the document author has recommended that the document be opened as readonly in C#.
type: docs
weight: 20
url: /net/aspose.words.settings/writeprotection/readonlyrecommended/
---
## WriteProtection.ReadOnlyRecommended property

Specifies whether the document author has recommended that the document be opened as read-only.

```csharp
public bool ReadOnlyRecommended { get; set; }
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

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);
Assert.IsTrue(doc.WriteProtection.ValidatePassword("MyPassword"));

// Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
doc.Save(ArtifactsDir + "Document.WriteProtection.docx");
doc = new Document(ArtifactsDir + "Document.WriteProtection.docx");

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);

builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln("Writing text in a protected document.");

Assert.AreEqual("Hello world! This document is protected." +
                "\rWriting text in a protected document.", doc.GetText().Trim());
```

### See Also

* class [WriteProtection](../)
* namespace [Aspose.Words.Settings](../../writeprotection/)
* assembly [Aspose.Words](../../../)
