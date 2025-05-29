---
title: XmlDsigLevel Enum
linktitle: XmlDsigLevel
articleTitle: XmlDsigLevel
second_title: Aspose.Words per .NET
description: Esplora l'enum Aspose.Words.DigitalSignatures.XmlDsigLevel per migliorare le tue firme digitali con gli standard XMLDSig per un'integrità dei documenti sicura e affidabile.
type: docs
weight: 630
url: /it/net/aspose.words.digitalsignatures/xmldsiglevel/
---
## XmlDsigLevel enumeration

Specifica il livello di una firma digitale basata sullo standard XML-DSig.

```csharp
public enum XmlDsigLevel
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| XmlDSig | `0` | Specifica il livello di firma XML-DSig. |
| XAdEsEpes | `1` | Specifica il livello di firma XAdES-EPES. |

## Esempi

Mostra come firmare documenti basati sullo standard XML-DSig.

```csharp
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
SignOptions signOptions = new SignOptions { XmlDsigLevel = XmlDsigLevel.XAdEsEpes };

string inputFileName = MyDir + "Document.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.XmlDsig.docx";
DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../)
