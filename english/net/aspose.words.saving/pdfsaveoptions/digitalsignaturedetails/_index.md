---
title: PdfSaveOptions.DigitalSignatureDetails
linktitle: DigitalSignatureDetails
articleTitle: DigitalSignatureDetails
second_title: Aspose.Words for .NET
description: Discover PdfSaveOptions DigitalSignatureDetails to easily manage PDF signing details, ensuring secure and efficient document output.
type: docs
weight: 80
url: /net/aspose.words.saving/pdfsaveoptions/digitalsignaturedetails/
---
## PdfSaveOptions.DigitalSignatureDetails property

Gets or sets the details for signing the output PDF document.

```csharp
public PdfDigitalSignatureDetails DigitalSignatureDetails { get; set; }
```

## Remarks

The default value is `null` and the output document will not be signed. When this property is set to a valid [`PdfDigitalSignatureDetails`](../../pdfdigitalsignaturedetails/) object, then the output PDF document will be digitally signed.

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

### See Also

* class [PdfDigitalSignatureDetails](../../pdfdigitalsignaturedetails/)
* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
