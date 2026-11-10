---
title: PdfDigitalSignatureHashAlgorithm Enum
linktitle: PdfDigitalSignatureHashAlgorithm
articleTitle: PdfDigitalSignatureHashAlgorithm
second_title: Aspose.Words for .NET
description: Explore the Aspose.Words PdfDigitalSignatureHashAlgorithm enum, defining digital hash algorithms for secure digital signatures in your documents.
type: docs
weight: 6350
url: /net/aspose.words.saving/pdfdigitalsignaturehashalgorithm/
---
## PdfDigitalSignatureHashAlgorithm enumeration

Specifies a digital hash algorithm used by a digital signature.

```csharp
public enum PdfDigitalSignatureHashAlgorithm
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Sha256 | `0` | SHA-256 hash algorithm. |
| Sha384 | `1` | SHA-384 hash algorithm. |
| Sha512 | `2` | SHA-512 hash algorithm. |
| RipeMD160 | `3` | RIPEMD-160 hash algorithm. |
| Auto | `4` | Automatically selects an appropriate hash algorithm based on the provided private key. |

## Examples

Shows how to sign a generated PDF document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Configure the "DigitalSignatureDetails" object of the "SaveOptions" object to
// digitally sign the document as we render it with the "Save" method.
DateTime signingTime = new DateTime(2015, 7, 20);
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime);
options.DigitalSignatureDetails.HashAlgorithm = PdfDigitalSignatureHashAlgorithm.RipeMD160;

Assert.That(options.DigitalSignatureDetails.Reason, Is.EqualTo("Test Signing"));
Assert.That(options.DigitalSignatureDetails.Location, Is.EqualTo("My Office"));
Assert.That(options.DigitalSignatureDetails.SignatureDate.ToLocalTime(), Is.EqualTo(signingTime));
Assert.That(options.DigitalSignatureDetails.CertificateHolder, Is.EqualTo(certificateHolder));

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

Shows how to sign a PDF document with a hash algorithm selected automatically based on the private key.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Contents of signed PDF.");

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

PdfSaveOptions options = new PdfSaveOptions();
options.DigitalSignatureDetails =
    new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", DateTime.Now);

// "Auto" is the default value. Some newer digital signature algorithms have specific digest requirements,
// so Aspose.Words picks a hash algorithm that is compatible with the certificate's private key.
Assert.That(options.DigitalSignatureDetails.HashAlgorithm, Is.EqualTo(PdfDigitalSignatureHashAlgorithm.Auto));

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureAutoHashAlgorithm.pdf", options);
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
