---
title: PdfDigitalSignatureDetails.PdfDigitalSignatureDetails
second_title: Aspose.Words för .NET API Referens
description: PdfDigitalSignatureDetails byggare. Initierar en instans av denna klass.
type: docs
weight: 10
url: /sv/net/aspose.words.saving/pdfdigitalsignaturedetails/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails() {#constructor}

Initierar en instans av denna klass.

```csharp
public PdfDigitalSignatureDetails()
```

### Exempel

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
DateTime signingTime = DateTime.Now;
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.Sha256;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime.ToUniversalTime(), options.DigitalSignatureDetails.SignatureDate.ToUniversalTime());

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### Se även

* class [PdfDigitalSignatureDetails](../)
* namnutrymme [Aspose.Words.Saving](../../pdfdigitalsignaturedetails/)
* hopsättning [Aspose.Words](../../../)

---

## PdfDigitalSignatureDetails(CertificateHolder, string, string, DateTime) {#constructor_1}

Initierar en instans av denna klass.

```csharp
public PdfDigitalSignatureDetails(CertificateHolder certificateHolder, string reason, 
    string location, DateTime signatureDate)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| certificateHolder | CertificateHolder | En certifikatinnehavare som innehåller själva certifikatet. |
| reason | String | Anledningen till undertecknandet. |
| location | String | Platsen för signering. |
| signatureDate | DateTime | Datum och tid för undertecknandet. |

### Exempel

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
DateTime signingTime = DateTime.Now;
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.Sha256;

Assert.AreEqual("Test Signing", options.DigitalSignatureDetails.Reason);
Assert.AreEqual("My Office", options.DigitalSignatureDetails.Location);
Assert.AreEqual(signingTime.ToUniversalTime(), options.DigitalSignatureDetails.SignatureDate.ToUniversalTime());

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

### Se även

* class [CertificateHolder](../../../aspose.words.digitalsignatures/certificateholder/)
* class [PdfDigitalSignatureDetails](../)
* namnutrymme [Aspose.Words.Saving](../../pdfdigitalsignaturedetails/)
* hopsättning [Aspose.Words](../../../)


