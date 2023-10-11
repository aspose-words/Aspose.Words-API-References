---
title: WriteProtection.ReadOnlyRecommended
second_title: Aspose.Words för .NET API Referens
description: WriteProtection fast egendom. Anger om dokumentförfattaren har rekommenderat att dokumentet öppnas som skrivskyddat.
type: docs
weight: 20
url: /sv/net/aspose.words.settings/writeprotection/readonlyrecommended/
---
## WriteProtection.ReadOnlyRecommended property

Anger om dokumentförfattaren har rekommenderat att dokumentet öppnas som skrivskyddat.

```csharp
public bool ReadOnlyRecommended { get; set; }
```

### Exempel

Visar hur man skyddar ett dokument med ett lösenord.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This document is protected.");
// Ange ett lösenord på upp till 15 tecken och verifiera sedan dokumentets skyddsstatus.
doc.WriteProtection.SetPassword("MyPassword");
doc.WriteProtection.ReadOnlyRecommended = true;

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);
Assert.IsTrue(doc.WriteProtection.ValidatePassword("MyPassword"));

// Skyddet hindrar inte dokumentet från att redigeras programmatiskt, och det krypterar inte heller innehållet.
doc.Save(ArtifactsDir + "Document.WriteProtection.docx");
doc = new Document(ArtifactsDir + "Document.WriteProtection.docx");

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);

builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln("Writing text in a protected document.");

Assert.AreEqual("Hello world! This document is protected." +
                "\rWriting text in a protected document.", doc.GetText().Trim());
```

### Se även

* class [WriteProtection](../)
* namnutrymme [Aspose.Words.Settings](../../writeprotection/)
* hopsättning [Aspose.Words](../../../)


