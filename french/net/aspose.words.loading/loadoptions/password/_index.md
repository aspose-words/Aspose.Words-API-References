---
title: LoadOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words pour .NET
description: LoadOptions Password propriété. Obtient ou définit le mot de passe pour ouvrir un document crypté. Peut êtrenul ou une chaîne vide. La valeur par défaut estnul  en C#.
type: docs
weight: 110
url: /fr/net/aspose.words.loading/loadoptions/password/
---
## LoadOptions.Password property

Obtient ou définit le mot de passe pour ouvrir un document crypté. Peut être`nul` ou une chaîne vide. La valeur par défaut est`nul` .

```csharp
public string Password { get; set; }
```

## Remarques

Vous devez connaître le mot de passe pour ouvrir un document crypté. Si le document n'est pas crypté, définissez-le sur`nul` ou une chaîne vide.

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

// Définit un nom de fichier système local pour le document d'entrée non signé et un nom de fichier de sortie pour sa nouvelle copie signée numériquement.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### Voir également

* class [LoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
