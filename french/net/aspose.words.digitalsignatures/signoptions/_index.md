---
title: SignOptions Class
linktitle: SignOptions
articleTitle: SignOptions
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.DigitalSignatures.SignOptions pour personnaliser votre processus de signature de documents avec des options flexibles et sécurisées pour un flux de travail amélioré.
type: docs
weight: 620
url: /fr/net/aspose.words.digitalsignatures/signoptions/
---
## SignOptions class

Permet de spécifier les options de signature des documents.

Pour en savoir plus, visitez le[Travailler avec des signatures numériques](https://docs.aspose.com/words/net/working-with-digital-signatures/) article de documentation.

```csharp
public class SignOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [SignOptions](signoptions/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [Comments](../../aspose.words.digitalsignatures/signoptions/comments/) { get; set; } | Spécifie les commentaires sur la signature numérique. La valeur par défaut est**chaîne vide**(Empty ). |
| [DecryptionPassword](../../aspose.words.digitalsignatures/signoptions/decryptionpassword/) { get; set; } | Le mot de passe pour décrypter le document source. La valeur par défaut est**chaîne vide** (Empty ). |
| [ProviderId](../../aspose.words.digitalsignatures/signoptions/providerid/) { get; set; } | Spécifie l'ID de classe du fournisseur de signature. La valeur par défaut est**Guid vide (tous les zéros)** . |
| [SignatureLineId](../../aspose.words.digitalsignatures/signoptions/signaturelineid/) { get; set; } | Identifiant de la ligne de signature. La valeur par défaut est**Guid vide (tous les zéros)** . |
| [SignatureLineImage](../../aspose.words.digitalsignatures/signoptions/signaturelineimage/) { get; set; } | L'image qui sera affichée dans l'association[`SignatureLine`](../../aspose.words.drawing/signatureline/) . La valeur par défaut est`nul` . |
| [SignTime](../../aspose.words.digitalsignatures/signoptions/signtime/) { get; set; } | La date de signature. La valeur par défaut est**heure actuelle** (Now) |
| [XmlDsigLevel](../../aspose.words.digitalsignatures/signoptions/xmldsiglevel/) { get; set; } | Spécifie le niveau d'une signature numérique basée sur la norme XML-DSig. La valeur par défaut estXmlDSig . |

## Exemples

Montre comment signer numériquement des documents.

```csharp
// Créez un certificat X.509 à partir d'un magasin PKCS#12, qui doit contenir une clé privée.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Créez un commentaire et une date qui seront appliqués avec notre nouvelle signature numérique.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Prendre un document non signé du système de fichiers local via un flux de fichiers,
// puis créez une copie signée de celui-ci déterminée par le nom de fichier du flux de fichiers de sortie.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Voir également

* espace de noms [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* Assemblée [Aspose.Words](../../)
