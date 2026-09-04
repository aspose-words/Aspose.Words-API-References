---
title: DigitalSignatureTimestampSettings.ServerUrl
linktitle: ServerUrl
articleTitle: ServerUrl
second_title: Aspose.Words for .NET
description: DigitalSignatureTimestampSettings ServerUrl property. Gets or sets a string value representing timestamp server URL. The default value is null.
type: docs
weight: 30
url: /net/aspose.words.digitalsignatures/digitalsignaturetimestampsettings/serverurl/
---
## DigitalSignatureTimestampSettings.ServerUrl property

Gets or sets a string value representing timestamp server URL. The default value is `null`.

```csharp
public string ServerUrl { get; set; }
```

## Remarks

If `null`, then the digital signature will not be time-stamped.

## Examples

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

* class [DigitalSignatureTimestampSettings](../)
* namespace [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assembly [Aspose.Words](../../../)
