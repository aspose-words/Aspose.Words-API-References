---
title: LoadOptions.Password
second_title: Référence de l'API Aspose.Words pour .NET
description: LoadOptions propriété. Obtient ou définit le mot de passe pour ouvrir un document chiffré. Peut être une chaîne nulle ou vide. La valeur par défaut est null.
type: docs
weight: 110
url: /fr/net/aspose.words.loading/loadoptions/password/
---
## LoadOptions.Password property

Obtient ou définit le mot de passe pour ouvrir un document chiffré. Peut être une chaîne nulle ou vide. La valeur par défaut est null.

```csharp
public string Password { get; set; }
```

### Remarques

Vous devez connaître le mot de passe pour ouvrir un document crypté. Si le document n'est pas crypté, définissez-le sur une chaîne nulle ou vide.

### Exemples

Montre comment signer un fichier de document crypté.

```csharp
// Crée un certificat X.509 à partir d'un magasin PKCS#12, qui doit contenir une clé privée.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Créez un commentaire, une date et un mot de passe de déchiffrement qui seront appliqués avec notre nouvelle signature numérique.
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

* class [LoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../loadoptions/)
* Assemblée [Aspose.Words](../../../)


