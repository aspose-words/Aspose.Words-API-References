---
title: SignOptions.XmlDsigLevel
linktitle: XmlDsigLevel
articleTitle: XmlDsigLevel
second_title: .NET için Aspose.Words
description: SignOptions'daki XmlDsigLevel özelliğini keşfedin ve dijital imza gücünü XMLDSig standartlarına göre tanımlayın. Güvenli ve güvenilir imzalar sağlayın!
type: docs
weight: 80
url: /tr/net/aspose.words.digitalsignatures/signoptions/xmldsiglevel/
---
## SignOptions.XmlDsigLevel property

XML-DSig standardına dayalı bir dijital imzanın düzeyini belirtir. Varsayılan değerXmlDSig .

```csharp
public XmlDsigLevel XmlDsigLevel { get; set; }
```

## Notlar

Office 2010'dan başlayarak farklı düzeylerde XAdES imzaları oluşturulabilir.

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

* enum [XmlDsigLevel](../../xmldsiglevel/)
* class [SignOptions](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)
