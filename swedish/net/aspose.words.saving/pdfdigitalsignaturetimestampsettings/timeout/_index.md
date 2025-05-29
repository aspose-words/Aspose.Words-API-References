---
title: PdfDigitalSignatureTimestampSettings.Timeout
linktitle: Timeout
articleTitle: Timeout
second_title: Aspose.Words för .NET
description: Optimera din PdfDigitalSignature med anpassningsbara Timeout-inställningar för sömlös åtkomst till tidsstämpelservrar. Förbättra säkerheten och effektiviteten idag!
type: docs
weight: 40
url: /sv/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/timeout/
---
## PdfDigitalSignatureTimestampSettings.Timeout property

Timeout-värde för åtkomst till tidsstämpelservern.

```csharp
public TimeSpan Timeout { get; set; }
```

## Anmärkningar

Standardvärdet är 100 sekunder.

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

* class [PdfDigitalSignatureTimestampSettings](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
