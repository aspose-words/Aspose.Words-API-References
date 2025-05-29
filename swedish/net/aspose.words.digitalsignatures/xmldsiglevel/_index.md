---
title: XmlDsigLevel Enum
linktitle: XmlDsigLevel
articleTitle: XmlDsigLevel
second_title: Aspose.Words för .NET
description: Utforska Aspose.Words.DigitalSignatures.XmlDsigLevel enum för att förbättra dina digitala signaturer med XMLDSig-standarder för säker och tillförlitlig dokumentintegritet.
type: docs
weight: 630
url: /sv/net/aspose.words.digitalsignatures/xmldsiglevel/
---
## XmlDsigLevel enumeration

Anger nivån på en digital signatur baserad på XML-DSig-standarden.

```csharp
public enum XmlDsigLevel
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| XmlDSig | `0` | Anger XML-DSig-signaturnivå. |
| XAdEsEpes | `1` | Anger XAdES-EPES signaturnivå. |

## Exempel

Visar hur man signerar dokument baserat på XML-DSig-standarden.

```csharp
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
SignOptions signOptions = new SignOptions { XmlDsigLevel = XmlDsigLevel.XAdEsEpes };

string inputFileName = MyDir + "Document.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.XmlDsig.docx";
DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### Se även

* namnutrymme [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../)
