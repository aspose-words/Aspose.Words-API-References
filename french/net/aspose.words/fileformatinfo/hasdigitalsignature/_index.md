---
title: FileFormatInfo.HasDigitalSignature
linktitle: HasDigitalSignature
articleTitle: HasDigitalSignature
second_title: Aspose.Words pour .NET
description: FileFormatInfo HasDigitalSignature propriété. Retoursvraisi ce document contient une signature numérique. Cette propriété informe simplement quune signature numérique est présente sur un document mais elle ne précise pas si la signature est valide ou non en C#.
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

Cette propriété existe pour vous aider à trier les documents signés numériquement de ceux qui ne le sont pas. Si vous utilisez Aspose.Words pour modifier et enregistrer un document signé numériquement, la signature numérique sera perdue. C'est intentionnel car une signature numérique existe pour protéger l'authenticité d'un document. En utilisant cette propriété, vous pouvez détecter les documents signés numériquement avant de les traiter de la même manière que les documents normaux et prendre certaines mesures pour éviter de perdre la signature numérique, par exemple en informer l'utilisateur.

## Exemples

Montre comment utiliser la classe FileFormatUtil pour détecter le format du document et la présence de signatures numériques.

```csharp
// Utilisez une instance FileFormatInfo pour vérifier qu'un document n'est pas signé numériquement.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, new SignOptions() { SignTime = DateTime.Now });

// Utilisez un nouveau FileFormatInstance pour confirmer qu'il est signé.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// Nous pouvons charger et accéder aux signatures d'un document signé dans une collection comme celle-ci.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### Voir également

* class [FileFormatInfo](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
