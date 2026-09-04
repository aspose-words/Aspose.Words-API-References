---
title: SignOptions.XmlDsigLevel
linktitle: XmlDsigLevel
articleTitle: XmlDsigLevel
second_title: Aspose.Words for .NET
description: Discover the XmlDsigLevel property in SignOptions, defining digital signature strength per XMLDSig standards. Ensure secure and reliable signatures!
type: docs
weight: 150
url: /net/aspose.words.digitalsignatures/signoptions/xmldsiglevel/
---
## SignOptions.XmlDsigLevel property

Specifies the level of a digital signature based on the XML-DSig standard. The default value is XmlDSig.

```csharp
public XmlDsigLevel XmlDsigLevel { get; set; }
```

## Remarks

Different levels of XAdES signatures can be created starting with Office 2010.

This is only relevant for the following document formats: DOC, DOCX, and XPS. It is ignored in other document formats, which always produce a plain XML-DSig signature regardless of this setting.

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
