---
title: XmlDsigLevel Enum
linktitle: XmlDsigLevel
articleTitle: XmlDsigLevel
second_title: Aspose.Words for .NET
description: Aspose.Words.DigitalSignatures.XmlDsigLevel enum. Specifies the level of a digital signature based on XMLDSig standard in C#.
type: docs
weight: 600
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

## Examples

Shows how to sign document based on XML-DSig standard.

```csharp
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
SignOptions signOptions = new SignOptions { XmlDsigLevel = XmlDsigLevel.XAdEsEpes };

string inputFileName = MyDir + "Document.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.XmlDsig.docx";
DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### See Also

* namespace [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* assembly [Aspose.Words](../../)
