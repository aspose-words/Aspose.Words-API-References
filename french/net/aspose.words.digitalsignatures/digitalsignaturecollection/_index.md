---
title: Class DigitalSignatureCollection
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.DigitalSignatures.DigitalSignatureCollection classe. Fournit une collection en lecture seule de signatures numériques jointes à un document.
type: docs
weight: 380
url: /fr/net/aspose.words.digitalsignatures/digitalsignaturecollection/
---
## DigitalSignatureCollection class

Fournit une collection en lecture seule de signatures numériques jointes à un document.

```csharp
public class DigitalSignatureCollection : IEnumerable<DigitalSignature>
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [DigitalSignatureCollection](digitalsignaturecollection/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.digitalsignatures/digitalsignaturecollection/count/) { get; } | Obtient le nombre d'éléments contenus dans la collection. |
| [IsValid](../../aspose.words.digitalsignatures/digitalsignaturecollection/isvalid/) { get; } | Retours`vrai` si toutes les signatures numériques de cette collection sont valides et que le document n'a pas été falsifié Renvoie également`vrai`s'il n'y a pas de signatures numériques. Renvoie`faux` si au moins une signature numérique est invalide. |
| [Item](../../aspose.words.digitalsignatures/digitalsignaturecollection/item/) { get; } | Obtient une signature de document à l'index spécifié. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetEnumerator](../../aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/)() | Renvoie un objet énumérateur de dictionnaire qui peut être utilisé pour itérer sur tous les éléments de la collection. |

### Remarques

[`DigitalSignatures`](../../aspose.words/document/digitalsignatures/)

### Exemples

Montre comment valider et afficher des informations sur chaque signature dans un document.

```csharp
Document doc = new Document(MyDir + "Digitally signed.docx");

foreach (DigitalSignature signature in doc.DigitalSignatures)
{
    Console.WriteLine($"{(signature.IsValid ? "Valid" : "Invalid")} signature: ");
    Console.WriteLine($"\tReason:\t{signature.Comments}"); 
    Console.WriteLine($"\tType:\t{signature.SignatureType}");
    Console.WriteLine($"\tSign time:\t{signature.SignTime}");
    Console.WriteLine($"\tSubject name:\t{signature.CertificateHolder.Certificate.SubjectName}");
    Console.WriteLine($"\tIssuer name:\t{signature.CertificateHolder.Certificate.IssuerName.Name}");
    Console.WriteLine();
}
```

Montre comment signer des documents avec des certificats X.509.

```csharp
// Vérifie qu'un document n'est pas signé.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Crée un objet CertificateHolder à partir d'un fichier PKCS12, que nous utiliserons pour signer le document.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Il existe deux manières d'enregistrer une copie signée d'un document dans le système de fichiers local :
// 1 - Désignez un document par un nom de fichier système local et enregistrez une copie signée à un emplacement spécifié par un autre nom de fichier.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Extraire un document d'un flux et enregistrer une copie signée dans un autre flux.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Veuillez vérifier que toutes les signatures numériques du document sont valides et vérifiez leurs détails.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### Voir également

* class [DigitalSignature](../digitalsignature/)
* espace de noms [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* Assemblée [Aspose.Words](../../)


