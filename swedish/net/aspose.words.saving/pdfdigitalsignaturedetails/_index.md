---
title: PdfDigitalSignatureDetails Class
linktitle: PdfDigitalSignatureDetails
articleTitle: PdfDigitalSignatureDetails
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.PdfDigitalSignatureDetails för sömlös digital PDF-signering. Förbättra dokumentsäkerheten med enkel integration och robusta funktioner.
type: docs
weight: 6220
url: /sv/net/aspose.words.saving/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails class

Innehåller information om hur man signerar ett PDF-dokument med en digital signatur.

```csharp
public class PdfDigitalSignatureDetails
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor)() | Initierar en instans av denna klass. |
| [PdfDigitalSignatureDetails](pdfdigitalsignaturedetails/#constructor_1)(*[CertificateHolder](../../aspose.words.digitalsignatures/certificateholder/), string, string, DateTime*) | Initierar en instans av denna klass. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CertificateHolder](../../aspose.words.saving/pdfdigitalsignaturedetails/certificateholder/) { get; set; } | Returnerar certifikatinnehavarobjektet som innehåller certifikatet som användes för att signera dokumentet. |
| [HashAlgorithm](../../aspose.words.saving/pdfdigitalsignaturedetails/hashalgorithm/) { get; set; } | Hämtar eller ställer in hashalgoritmen. |
| [Location](../../aspose.words.saving/pdfdigitalsignaturedetails/location/) { get; set; } | Hämtar eller anger signeringens plats. |
| [Reason](../../aspose.words.saving/pdfdigitalsignaturedetails/reason/) { get; set; } | Hämtar eller anger orsaken till signeringen. |
| [SignatureDate](../../aspose.words.saving/pdfdigitalsignaturedetails/signaturedate/) { get; set; } | Hämtar eller ställer in datumet för signeringen. |
| [TimestampSettings](../../aspose.words.saving/pdfdigitalsignaturedetails/timestampsettings/) { get; set; } | Hämtar eller ställer in tidsstämpelinställningar för digitala signaturer. |

## Anmärkningar

För närvarande är digital signering av PDF-dokument endast tillgängligt på .NET 3.5 eller senare.

För att signera ett PDF-dokument digitalt när det skapas av Aspose.Words, ställ in[`DigitalSignatureDetails`](../pdfsaveoptions/digitalsignaturedetails/) egenskap till en giltig`PdfDigitalSignatureDetails` objektet och spara sedan dokumentet i PDF-formatet och skicka [`PdfSaveOptions`](../pdfsaveoptions/) som en parameter i[`Save`](../../aspose.words/document/save/) metod.

Aspose.Words skapar en PKCS#7-signatur över hela PDF-dokumentet och använder filtret "Adobe.PPKMS" och delfiltret "adbe.pkcs7.sha1" när en digital signatur skapas.

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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
