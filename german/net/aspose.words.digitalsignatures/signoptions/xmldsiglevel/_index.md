---
title: SignOptions.XmlDsigLevel
linktitle: XmlDsigLevel
articleTitle: XmlDsigLevel
second_title: Aspose.Words für .NET
description: Entdecken Sie die XmlDsigLevel-Eigenschaft in SignOptions, die die Stärke digitaler Signaturen gemäß XMLDSig-Standards definiert. Sorgen Sie für sichere und zuverlässige Signaturen!
type: docs
weight: 80
url: /de/net/aspose.words.digitalsignatures/signoptions/xmldsiglevel/
---
## SignOptions.XmlDsigLevel property

Gibt die Ebene einer digitalen Signatur basierend auf dem XML-DSig-Standard an. Der Standardwert istXmlDSig .

```csharp
public XmlDsigLevel XmlDsigLevel { get; set; }
```

## Bemerkungen

Ab Office 2010 können verschiedene Ebenen von XAdES-Signaturen erstellt werden.

## Beispiele

Zeigt, wie Dokumente basierend auf dem XML-DSig-Standard signiert werden.

```csharp
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
SignOptions signOptions = new SignOptions { XmlDsigLevel = XmlDsigLevel.XAdEsEpes };

string inputFileName = MyDir + "Document.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.XmlDsig.docx";
DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### Siehe auch

* enum [XmlDsigLevel](../../xmldsiglevel/)
* class [SignOptions](../)
* namensraum [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../../)
