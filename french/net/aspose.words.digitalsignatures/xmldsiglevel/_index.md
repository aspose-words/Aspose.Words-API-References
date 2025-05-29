---
title: XmlDsigLevel Enum
linktitle: XmlDsigLevel
articleTitle: XmlDsigLevel
second_title: Aspose.Words pour .NET
description: Explorez l'énumération Aspose.Words.DigitalSignatures.XmlDsigLevel pour améliorer vos signatures numériques avec les normes XMLDSig pour une intégrité de document sécurisée et fiable.
type: docs
weight: 630
url: /fr/net/aspose.words.digitalsignatures/xmldsiglevel/
---
## XmlDsigLevel enumeration

Spécifie le niveau d'une signature numérique basée sur la norme XML-DSig.

```csharp
public enum XmlDsigLevel
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| XmlDSig | `0` | Spécifie le niveau de signature XML-DSig. |
| XAdEsEpes | `1` | Spécifie le niveau de signature XAdES-EPES. |

## Exemples

Montre comment signer un document basé sur la norme XML-DSig.

```csharp
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
SignOptions signOptions = new SignOptions { XmlDsigLevel = XmlDsigLevel.XAdEsEpes };

string inputFileName = MyDir + "Document.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.XmlDsig.docx";
DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### Voir également

* espace de noms [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* Assemblée [Aspose.Words](../../)
