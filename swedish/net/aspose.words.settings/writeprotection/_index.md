---
title: WriteProtection Class
linktitle: WriteProtection
articleTitle: WriteProtection
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Settings.WriteProtection för att enkelt hantera inställningar för dokumentskrivskydd och förbättra din dokumentsäkerhet.
type: docs
weight: 6800
url: /sv/net/aspose.words.settings/writeprotection/
---
## WriteProtection class

Anger skrivskyddsinställningar för ett dokument.

För att lära dig mer, besök[Skydda eller kryptera ett dokument](https://docs.aspose.com/words/net/protect-or-encrypt-a-document/) dokumentationsartikel.

```csharp
public class WriteProtection
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [IsWriteProtected](../../aspose.words.settings/writeprotection/iswriteprotected/) { get; } | Returer`sann` när ett lösenord för skrivskydd är inställt. |
| [ReadOnlyRecommended](../../aspose.words.settings/writeprotection/readonlyrecommended/) { get; set; } | Anger om dokumentförfattaren har rekommenderat att dokumentet öppnas som skrivskyddat. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [SetPassword](../../aspose.words.settings/writeprotection/setpassword/)(*string*) | Ställer in lösenordet för skrivskydd för dokumentet. |
| [ValidatePassword](../../aspose.words.settings/writeprotection/validatepassword/)(*string*) | Returer`sann` om det angivna lösenordet är detsamma som skrivskyddslösenordet som dokumentet skyddades med. Om dokumentet inte är skrivskyddat med lösenord returneras`falsk` . |

## Anmärkningar

Skrivskydd anger om författaren har rekommenderat att dokumentet ska öppnas som skrivskyddat och/eller kräva ett lösenord för att ändra ett dokument.

Skrivskydd skiljer sig från dokumentskydd. Skrivskydd anges i Microsoft Word i alternativen i dialogrutan Spara som.

Du skapar inte instanser av den här klassen direkt. Du kommer åt dokumentskyddsinställningar via[`WriteProtection`](../../aspose.words/document/writeprotection/) egendom.

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

* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../)
