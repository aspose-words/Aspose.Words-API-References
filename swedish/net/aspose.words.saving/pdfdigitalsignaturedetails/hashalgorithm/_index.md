---
title: PdfDigitalSignatureDetails.HashAlgorithm
linktitle: HashAlgorithm
articleTitle: HashAlgorithm
second_title: Aspose.Words för .NET
description: PdfDigitalSignatureDetails HashAlgorithm fast egendom. Hämtar eller ställer in hashalgoritmen i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/pdfdigitalsignaturedetails/hashalgorithm/
---
## PdfDigitalSignatureDetails.HashAlgorithm property

Hämtar eller ställer in hash-algoritmen.

```csharp
public PdfDigitalSignatureHashAlgorithm HashAlgorithm { get; set; }
```

## Anmärkningar

Standardvärdet är SHA-256-algoritmen.

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

* enum [PdfDigitalSignatureHashAlgorithm](../../pdfdigitalsignaturehashalgorithm/)
* class [PdfDigitalSignatureDetails](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
