---
title: FileFormatInfo.HasDigitalSignature
linktitle: HasDigitalSignature
articleTitle: HasDigitalSignature
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FileFormatInfo HasDigitalSignature : vérifiez rapidement si votre document inclut une signature numérique, améliorant ainsi la sécurité et l'authenticité.
type: docs
weight: 20
url: /fr/net/aspose.words/fileformatinfo/hasdigitalsignature/
---
## FileFormatInfo.HasDigitalSignature property

Retours`vrai`si ce document contient une signature numérique. Cette propriété informe simplement qu'une signature numérique est présente sur un document, mais elle ne précise pas si la signature est valide ou non.

```csharp
public bool HasDigitalSignature { get; }
```

## Remarques

Cette propriété permet de trier les documents signés numériquement de ceux qui ne le sont pas. Si vous utilisez Aspose.Words pour modifier et enregistrer un document signé numériquement, la signature numérique sera perdue. Ceci est intentionnel, car une signature numérique sert à garantir l'authenticité d'un document. Cette propriété permet de détecter les documents signés numériquement avant de les traiter, comme pour les documents normaux, et de prendre des mesures pour éviter leur perte, par exemple en avertissant l'utilisateur.

## Exemples

Montre comment utiliser la classe FileFormatUtil pour détecter le format du document et la présence de signatures numériques.

```csharp
// Utilisez une instance FileFormatInfo pour vérifier qu'un document n'est pas signé numériquement.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
SignOptions signOptions = new SignOptions() { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, signOptions);

// Utilisez une nouvelle FileFormatInstance pour confirmer qu'elle est signée.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// Nous pouvons charger et accéder aux signatures d'un document signé dans une collection comme celle-ci.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### Voir également

* class [FileFormatInfo](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
