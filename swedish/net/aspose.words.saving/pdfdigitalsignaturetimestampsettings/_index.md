---
title: PdfDigitalSignatureTimestampSettings Class
linktitle: PdfDigitalSignatureTimestampSettings
articleTitle: PdfDigitalSignatureTimestampSettings
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.PdfDigitalSignatureTimestampSettings för sömlös hantering av tidsstämplar för digitala signaturer. Förbättra din PDF-säkerhet utan ansträngning!
type: docs
weight: 6240
url: /sv/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/
---
## PdfDigitalSignatureTimestampSettings class

Innehåller inställningar för tidsstämpeln för digital signatur.

För att lära dig mer, besök[Arbeta med digitala signaturer](https://docs.aspose.com/words/net/working-with-digital-signatures/) dokumentationsartikel.

```csharp
public class PdfDigitalSignatureTimestampSettings
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [PdfDigitalSignatureTimestampSettings](pdfdigitalsignaturetimestampsettings/#constructor)() | Initierar en instans av denna klass. |
| [PdfDigitalSignatureTimestampSettings](pdfdigitalsignaturetimestampsettings/#constructor_1)(*string, string, string*) | Initierar en instans av denna klass. |
| [PdfDigitalSignatureTimestampSettings](pdfdigitalsignaturetimestampsettings/#constructor_2)(*string, string, string, TimeSpan*) | Initierar en instans av denna klass. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Password](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/password/) { get; set; } | Lösenord för tidsstämpelserver. |
| [ServerUrl](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/serverurl/) { get; set; } | Tidsstämpelserverns URL. |
| [Timeout](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/timeout/) { get; set; } | Timeout-värde för åtkomst till tidsstämpelservern. |
| [UserName](../../aspose.words.saving/pdfdigitalsignaturetimestampsettings/username/) { get; set; } | Tidsstämpelserver användarnamn. |

## Exempel

Visar hur man signerar ett sparat PDF-dokument digitalt och tidsstämplar det.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Skapa en digital signatur och tilldela den till vårt SaveOptions-objekt för att signera dokumentet när vi sparar det som PDF.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// Skapa en tidsstämpel som verifierats av en tidsstämpel, auktoritetsverifierad.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "Mitt lösenord");

// Standardlivslängden för tidsstämpeln är 100 sekunder.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// Vi kan ställa in vår timeout-period via konstruktorn.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr", options.DigitalSignatureDetails.TimestampSettings.ServerUrl);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// Metoden "Spara" kommer att tillämpa vår signatur på utdatadokumentet vid denna tidpunkt.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
