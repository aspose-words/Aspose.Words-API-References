---
title: DigitalSignatureTimestampSettings Class
linktitle: DigitalSignatureTimestampSettings
articleTitle: DigitalSignatureTimestampSettings
second_title: Aspose.Words for .NET
description: Aspose.Words.DigitalSignatures.DigitalSignatureTimestampSettings class. Contains settings of the digital signature timestamp.
type: docs
weight: 600
url: /net/aspose.words.digitalsignatures/digitalsignaturetimestampsettings/
---
## DigitalSignatureTimestampSettings class

Contains settings of the digital signature timestamp.

```csharp
public class DigitalSignatureTimestampSettings
```

## Constructors

| Name | Description |
| --- | --- |
| [DigitalSignatureTimestampSettings](digitalsignaturetimestampsettings/#constructor)() | Initializes a new instance of `DigitalSignatureTimestampSettings` class. |
| [DigitalSignatureTimestampSettings](digitalsignaturetimestampsettings/#constructor_1)(*string, string, string*) | Initializes a new instance of `DigitalSignatureTimestampSettings` class. |
| [DigitalSignatureTimestampSettings](digitalsignaturetimestampsettings/#constructor_2)(*string, string, string, TimeSpan*) | Initializes a new instance of `DigitalSignatureTimestampSettings` class. |

## Properties

| Name | Description |
| --- | --- |
| [Password](../../aspose.words.digitalsignatures/digitalsignaturetimestampsettings/password/) { get; set; } | Gets or sets a string value representing timestamp server password. The default value is `null`. |
| [ServerUrl](../../aspose.words.digitalsignatures/digitalsignaturetimestampsettings/serverurl/) { get; set; } | Gets or sets a string value representing timestamp server URL. The default value is `null`. |
| [Timeout](../../aspose.words.digitalsignatures/digitalsignaturetimestampsettings/timeout/) { get; set; } | Gets or sets a time-out value for accessing timestamp server. The default value is 100 seconds. |
| [UserName](../../aspose.words.digitalsignatures/digitalsignaturetimestampsettings/username/) { get; set; } | Gets or sets a string value representing timestamp server user name. The default value is `null`. |

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

* namespace [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* assembly [Aspose.Words](../../)
