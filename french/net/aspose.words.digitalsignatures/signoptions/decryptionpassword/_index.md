---
title: SignOptions.DecryptionPassword
linktitle: DecryptionPassword
articleTitle: DecryptionPassword
second_title: Aspose.Words pour .NET
description: Déverrouillez vos documents sans effort grâce à la fonctionnalité DecryptionPassword de SignOptions. Décryptez facilement et en toute sécurité vos fichiers sources ; la valeur par défaut est une chaîne vide.
type: docs
weight: 30
url: /fr/net/aspose.words.digitalsignatures/signoptions/decryptionpassword/
---
## SignOptions.DecryptionPassword property

Le mot de passe pour décrypter le document source. La valeur par défaut est**chaîne vide** (Empty ).

```csharp
public string DecryptionPassword { get; set; }
```

## Remarques

Si le document OOXML est chiffré, vous devez fournir un mot de passe de déchiffrement pour déchiffrer le document source avant qu'il ne soit signé. Ceci n'est pas requis pour les documents au format binaire DOC.

## Exemples

Montre comment signer un fichier de document crypté.

```csharp
// Créez un certificat X.509 à partir d'un magasin PKCS#12, qui doit contenir une clé privée.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Créez un commentaire, une date et un mot de passe de décryptage qui seront appliqués avec notre nouvelle signature numérique.
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// Définissez un nom de fichier système local pour le document d'entrée non signé et un nom de fichier de sortie pour sa nouvelle copie signée numériquement.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### Voir également

* class [SignOptions](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Assemblée [Aspose.Words](../../../)
