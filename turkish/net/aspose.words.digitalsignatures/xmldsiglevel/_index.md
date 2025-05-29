---
title: XmlDsigLevel Enum
linktitle: XmlDsigLevel
articleTitle: XmlDsigLevel
second_title: .NET için Aspose.Words
description: Dijital imzalarınızı güvenli ve güvenilir belge bütünlüğü için XMLDSig standartlarıyla geliştirmek üzere Aspose.Words.DigitalSignatures.XmlDsigLevel enum'unu keşfedin.
type: docs
weight: 630
url: /tr/net/aspose.words.digitalsignatures/xmldsiglevel/
---
## XmlDsigLevel enumeration

XML-DSig standardına dayalı bir dijital imzanın seviyesini belirtir.

```csharp
public enum XmlDsigLevel
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| XmlDSig | `0` | XML-DSig imza düzeyini belirtir. |
| XAdEsEpes | `1` | XAdES-EPES imza düzeyini belirtir. |

## Örnekler

XML-DSig standardına göre belgenin nasıl imzalanacağını gösterir.

```csharp
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
SignOptions signOptions = new SignOptions { XmlDsigLevel = XmlDsigLevel.XAdEsEpes };

string inputFileName = MyDir + "Document.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.XmlDsig.docx";
DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../)
