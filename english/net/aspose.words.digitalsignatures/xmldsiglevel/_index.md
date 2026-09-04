---
title: XmlDsigLevel Enum
linktitle: XmlDsigLevel
articleTitle: XmlDsigLevel
second_title: Aspose.Words for .NET
description: Explore Aspose.Words.DigitalSignatures.XmlDsigLevel enum to enhance your digital signatures with XMLDSig standards for secure and reliable document integrity.
type: docs
weight: 640
url: /net/aspose.words.digitalsignatures/xmldsiglevel/
---
## XmlDsigLevel enumeration

Specifies the level of a digital signature based on XML-DSig standard.

```csharp
public enum XmlDsigLevel
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| XmlDSig | `0` | Specifies XML-DSig signature level. |
| XAdEsEpes | `1` | Specifies XAdES-EPES signature level. |
| XAdEsT | `2` | Specifies XAdES-T signature level. |

## Examples

Shows how to sign document based on XML-DSig standard.

```csharp
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
SignOptions signOptions = new SignOptions { XmlDsigLevel = XmlDsigLevel.XAdEsEpes };

string inputFileName = MyDir + "Document.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.XmlDsig.docx";
DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

Shows how to sign a document with timestamping using DigitalSignatureUtil.

```csharp
SignOptions signOptions = new SignOptions
{
    XmlDsigLevel = XmlDsigLevel.XAdEsT,
    TimestampSettings = new DigitalSignatureTimestampSettings(
        "https://freetsa.org/tsr",
        "JohnDoe",
        "MyPassword")
};

CertificateHolder cert = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

DigitalSignatureUtil.Sign(MyDir + "Digitally signed.docx", ArtifactsDir + "DigitalSignatureUtil.Timestamped.docx", cert, signOptions);

Document signedDoc = new Document(ArtifactsDir + "DigitalSignatureUtil.Timestamped.docx");

Assert.That(signedDoc.DigitalSignatures.Count, Is.EqualTo(1));
Assert.That(signedDoc.DigitalSignatures[0].IsValid, Is.True);

// Verify timestamp settings are applied.
Assert.That(signOptions.TimestampSettings.ServerUrl, Is.EqualTo("https://freetsa.org/tsr"));
Assert.That(signOptions.TimestampSettings.UserName, Is.EqualTo("JohnDoe"));
Assert.That(signOptions.TimestampSettings.Password, Is.EqualTo("MyPassword"));
Assert.That(signOptions.TimestampSettings.Timeout.TotalSeconds, Is.EqualTo(100.0d));

// Test with custom timeout.
signOptions.TimestampSettings = new DigitalSignatureTimestampSettings(
    "https://freetsa.org/tsr",
    "JohnDoe",
    "MyPassword",
    TimeSpan.FromMinutes(30));

Assert.That(signOptions.TimestampSettings.Timeout.TotalSeconds, Is.EqualTo(1800.0d));
```

### See Also

* namespace [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* assembly [Aspose.Words](../../)
