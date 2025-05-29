---
title: SignOptions.XmlDsigLevel
linktitle: XmlDsigLevel
articleTitle: XmlDsigLevel
second_title: Aspose.Words för .NET
description: Upptäck egenskapen XmlDsigLevel i SignOptions, som definierar digital signaturstyrka enligt XMLDSig-standarder. Säkerställ säkra och tillförlitliga signaturer!
type: docs
weight: 80
url: /sv/net/aspose.words.digitalsignatures/signoptions/xmldsiglevel/
---
## SignOptions.XmlDsigLevel property

Anger nivån för en digital signatur baserat på XML-DSig-standarden. Standardvärdet ärXmlDSig .

```csharp
public XmlDsigLevel XmlDsigLevel { get; set; }
```

## Anmärkningar

Olika nivåer av XAdES-signaturer kan skapas från och med Office 2010.

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

* enum [XmlDsigLevel](../../xmldsiglevel/)
* class [SignOptions](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../../)
