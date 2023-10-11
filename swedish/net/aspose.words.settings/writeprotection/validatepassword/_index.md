---
title: WriteProtection.ValidatePassword
second_title: Aspose.Words för .NET API Referens
description: WriteProtection metod. ReturnerarSann om det angivna lösenordet är detsamma som skrivskyddslösenordet som dokumentet skyddades med. Om dokumentet inte är skrivskyddat med lösenord returnerasfalsk .
type: docs
weight: 40
url: /sv/net/aspose.words.settings/writeprotection/validatepassword/
---
## WriteProtection.ValidatePassword method

Returnerar`Sann` om det angivna lösenordet är detsamma som skrivskyddslösenordet som dokumentet skyddades med. Om dokumentet inte är skrivskyddat med lösenord returneras`falsk` .

```csharp
public bool ValidatePassword(string password)
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


