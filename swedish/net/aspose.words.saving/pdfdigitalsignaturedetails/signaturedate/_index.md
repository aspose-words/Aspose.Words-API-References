---
title: PdfDigitalSignatureDetails.SignatureDate
linktitle: SignatureDate
articleTitle: SignatureDate
second_title: Aspose.Words för .NET
description: PdfDigitalSignatureDetails SignatureDate fast egendom. Hämtar eller ställer in datumet för signeringen i C#.
type: docs
weight: 60
url: /sv/net/aspose.words.saving/pdfdigitalsignaturedetails/signaturedate/
---
## PdfDigitalSignatureDetails.SignatureDate property

Hämtar eller ställer in datumet för signeringen.

```csharp
public DateTime SignatureDate { get; set; }
```

## Anmärkningar

Standardvärdet är den aktuella tiden.

Detta värde kommer att visas i den digitala signaturen som en overifierad datortid.

## Exempel

Visar hur man signerar ett genererat PDF-dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Konfigurera "DigitalSignatureDetails"-objektet för "SaveOptions"-objektet till
// signera dokumentet digitalt när vi renderar det med "Spara"-metoden.
DateTime signingTime = new DateTime(2015, 7, 20);
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.RipeMD160;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime, options.DigitalSignatureDetails.SignatureDate.ToLocalTime());

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### Se även

* class [PdfDigitalSignatureDetails](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
