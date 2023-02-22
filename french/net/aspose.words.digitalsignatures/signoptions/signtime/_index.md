---
title: SignOptions.SignTime
second_title: Référence de l'API Aspose.Words pour .NET
description: SignOptions propriété. La date de signature. La valeur par défaut est heure actuelle Now .
type: docs
weight: 70
url: /fr/net/aspose.words.digitalsignatures/signoptions/signtime/
---
## SignOptions.SignTime property

La date de signature. La valeur par défaut est **heure actuelle** (Now ).

```csharp
public DateTime SignTime { get; set; }
```

### Exemples

Montre comment signer numériquement des documents.

```csharp
// Crée un certificat X.509 à partir d'un magasin PKCS#12, qui doit contenir une clé privée.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Créez un commentaire et une date qui seront appliqués avec notre nouvelle signature numérique.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Prend un document non signé du système de fichiers local via un flux de fichiers,
// puis créez une copie signée de celui-ci déterminée par le nom de fichier du flux de fichier de sortie.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Voir également

* class [SignOptions](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../signoptions/)
* Assemblée [Aspose.Words](../../../)


