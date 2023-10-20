---
title: PdfSaveOptions.DigitalSignatureDetails
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: Aspose.Words för .NET
description: PdfSaveOptions DigitalSignatureDetails fast egendom. Hämtar eller ställer in detaljerna för att signera PDFdokumentet i C#.
type: docs
weight: 70
url: /sv/net/aspose.words.saving/pdfsaveoptions/digitalsignaturedetails/
---
## PdfSaveOptions.DigitalSignatureDetails property

Hämtar eller ställer in detaljerna för att signera PDF-dokumentet.

```csharp
public PdfDigitalSignatureDetails DigitalSignatureDetails { get; set; }
```

## Anmärkningar

Standardvärdet är`null`och utdatadokumentet kommer inte att signeras. När denna egenskap är inställd på en giltig[`PdfDigitalSignatureDetails`](../../pdfdigitalsignaturedetails/) object, så kommer PDF-dokumentet att signeras digitalt.

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

* class [PdfDigitalSignatureDetails](../../pdfdigitalsignaturedetails/)
* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
