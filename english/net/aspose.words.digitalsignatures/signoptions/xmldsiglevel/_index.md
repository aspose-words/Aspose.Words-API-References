---
title: SignOptions.XmlDsigLevel
linktitle: XmlDsigLevel
articleTitle: XmlDsigLevel
second_title: Aspose.Words for .NET
description: SignOptions XmlDsigLevel property. Specifies the level of a digital signature based on XMLDSig standard. The default value is XmlDSig in C#.
type: docs
weight: 80
url: /net/aspose.words.digitalsignatures/signoptions/xmldsiglevel/
---
## SignOptions.XmlDsigLevel property

Specifies the level of a digital signature based on XML-DSig standard. The default value is XmlDSig.

```csharp
public XmlDsigLevel XmlDsigLevel { get; set; }
```

## Remarks

Different levels of XAdES signatures can be created starting from Office 2010.

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

* enum [XmlDsigLevel](../../xmldsiglevel/)
* class [SignOptions](../)
* namespace [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assembly [Aspose.Words](../../../)
