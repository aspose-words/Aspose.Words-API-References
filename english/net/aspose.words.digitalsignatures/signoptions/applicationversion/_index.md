---
title: SignOptions.ApplicationVersion
linktitle: ApplicationVersion
articleTitle: ApplicationVersion
second_title: Aspose.Words for .NET
description: Set or get app version for signing. Ensure compatibility and control signature metadata. Default 12.0.
type: docs
weight: 20
url: /net/aspose.words.digitalsignatures/signoptions/applicationversion/
---
## SignOptions.ApplicationVersion property

Gets or sets the application version for the digital signature. Default value is "12.0".

```csharp
public string ApplicationVersion { get; set; }
```

## Examples

Shows how to sign a document with additional signing options.

```csharp
SignOptions signOptions = new SignOptions()
{
    WindowsVersion = "10.0",
    ApplicationVersion = "16.0.19127",
    OfficeVersion = "16.0.19127/27",
    HorizontalResolution = 1024,
    VerticalResolution = 768,
    ColorDepth = 24
};

byte[] certBytes = File.ReadAllBytes(MyDir + "morzal.pfx");
CertificateHolder cert = CertificateHolder.Create(certBytes, "aw");
DigitalSignatureUtil.Sign(MyDir + "Digitally signed.docx", ArtifactsDir + "DigitalSignatureUtil.docx", cert, signOptions);

Document signedDoc = new Document(ArtifactsDir + "DigitalSignatureUtil.docx");

DigitalSignature signature = signedDoc.DigitalSignatures[0];
Assert.That(signedDoc.DigitalSignatures.Count, Is.EqualTo(1));
Assert.That(signature.IsValid, Is.True);
Assert.That(signature.WindowsVersion, Is.EqualTo("10.0"));
Assert.That(signature.ApplicationVersion, Is.EqualTo("16.0.19127"));
Assert.That(signature.OfficeVersion, Is.EqualTo("16.0.19127/27"));
Assert.That(signature.HorizontalResolution, Is.EqualTo(1024));
Assert.That(signature.VerticalResolution, Is.EqualTo(768));
Assert.That(signature.ColorDepth, Is.EqualTo(24));
```

### See Also

* class [SignOptions](../)
* namespace [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assembly [Aspose.Words](../../../)
