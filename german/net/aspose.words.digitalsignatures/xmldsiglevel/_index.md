---
title: XmlDsigLevel Enum
linktitle: XmlDsigLevel
articleTitle: XmlDsigLevel
second_title: Aspose.Words für .NET
description: Erkunden Sie die Aufzählung Aspose.Words.DigitalSignatures.XmlDsigLevel, um Ihre digitalen Signaturen mit XMLDSig-Standards für sichere und zuverlässige Dokumentintegrität zu verbessern.
type: docs
weight: 630
url: /de/net/aspose.words.digitalsignatures/xmldsiglevel/
---
## XmlDsigLevel enumeration

Gibt die Ebene einer digitalen Signatur basierend auf dem XML-DSig-Standard an.

```csharp
public enum XmlDsigLevel
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| XmlDSig | `0` | Gibt die XML-DSig-Signaturebene an. |
| XAdEsEpes | `1` | Gibt die Signaturebene von XAdES-EPES an. |

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

* namensraum [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../)
