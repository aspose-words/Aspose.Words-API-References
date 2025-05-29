---
title: Document.WriteProtection
linktitle: WriteProtection
articleTitle: WriteProtection
second_title: Aspose.Words för .NET
description: Utforska egenskapen Dokumentskrivskydd för att enkelt hantera dokumentets skrivskyddsinställningar och förbättra säkerheten.
type: docs
weight: 520
url: /sv/net/aspose.words/document/writeprotection/
---
## Document.WriteProtection property

Ger åtkomst till dokumentets skrivskyddsalternativ.

```csharp
public WriteProtection WriteProtection { get; }
```

## Exempel

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

// Skyddet hindrar inte dokumentet från att redigeras programmatiskt, och krypterar inte heller innehållet.
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

* class [WriteProtection](../../../aspose.words.settings/writeprotection/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
