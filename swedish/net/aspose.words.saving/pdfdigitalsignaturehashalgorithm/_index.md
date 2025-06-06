---
title: PdfDigitalSignatureHashAlgorithm Enum
linktitle: PdfDigitalSignatureHashAlgorithm
articleTitle: PdfDigitalSignatureHashAlgorithm
second_title: Aspose.Words för .NET
description: Utforska Aspose.Words PdfDigitalSignatureHashAlgorithm-uppräkningen, som definierar digitala hashalgoritmer för säkra digitala signaturer i dina dokument.
type: docs
weight: 6230
url: /sv/net/aspose.words.saving/pdfdigitalsignaturehashalgorithm/
---
## PdfDigitalSignatureHashAlgorithm enumeration

Anger en digital hashalgoritm som används av en digital signatur.

```csharp
public enum PdfDigitalSignatureHashAlgorithm
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Sha256 | `0` | SHA-256 hash-algoritm. |
| Sha384 | `1` | SHA-384 hash-algoritm. |
| Sha512 | `2` | SHA-512 hash-algoritm. |
| RipeMD160 | `3` | RIPEMD-160 hash-algoritm. |

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
