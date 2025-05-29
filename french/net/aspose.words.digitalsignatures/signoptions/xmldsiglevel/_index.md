---
title: SignOptions.XmlDsigLevel
linktitle: XmlDsigLevel
articleTitle: XmlDsigLevel
second_title: Aspose.Words pour .NET
description: Découvrez la propriété XmlDsigLevel dans SignOptions, qui définit la force des signatures numériques selon les normes XMLDSig. Assurez des signatures sécurisées et fiables !
type: docs
weight: 80
url: /fr/net/aspose.words.digitalsignatures/signoptions/xmldsiglevel/
---
## SignOptions.XmlDsigLevel property

Spécifie le niveau d'une signature numérique basée sur la norme XML-DSig. La valeur par défaut estXmlDSig .

```csharp
public XmlDsigLevel XmlDsigLevel { get; set; }
```

## Remarques

Différents niveaux de signatures XAdES peuvent être créés à partir d'Office 2010.

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

* enum [XmlDsigLevel](../../xmldsiglevel/)
* class [SignOptions](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Assemblée [Aspose.Words](../../../)
