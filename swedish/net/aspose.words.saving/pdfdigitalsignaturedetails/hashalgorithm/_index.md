---
title: PdfDigitalSignatureDetails.HashAlgorithm
linktitle: HashAlgorithm
articleTitle: HashAlgorithm
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PdfDigitalSignatureDetails HashAlgorithm – hantera och anpassa dina hashalgoritmer effektivt för förbättrad digital säkerhet.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/pdfdigitalsignaturedetails/hashalgorithm/
---
## PdfDigitalSignatureDetails.HashAlgorithm property

Hämtar eller ställer in hashalgoritmen.

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

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Konfigurera objektet "DigitalSignatureDetails" för objektet "SaveOptions" till
// signera dokumentet digitalt när vi renderar det med metoden "Spara".
DateTime signingTime = new DateTime(2015, 7, 20);
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.RipeMD160;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime, options.DigitalSignatureDetails.SignatureDate.ToLocalTime());
Assert.AreEqual(certificateHolder, options.DigitalSignatureDetails.CertificateHolder);

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### Se även

* enum [PdfDigitalSignatureHashAlgorithm](../../pdfdigitalsignaturehashalgorithm/)
* class [PdfDigitalSignatureDetails](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
