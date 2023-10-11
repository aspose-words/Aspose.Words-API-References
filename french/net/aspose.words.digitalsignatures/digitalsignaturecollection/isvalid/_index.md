---
title: DigitalSignatureCollection.IsValid
second_title: Référence de l'API Aspose.Words pour .NET
description: DigitalSignatureCollection propriété. Retoursvrai si toutes les signatures numériques de cette collection sont valides et que le document na pas été falsifié with Renvoie égalementvrai sil ny a pas de signatures numériques. FAUX si au moins une signature numérique est invalide.
type: docs
weight: 30
url: /fr/net/aspose.words.digitalsignatures/digitalsignaturecollection/isvalid/
---
## DigitalSignatureCollection.IsValid property

Retours`vrai` si toutes les signatures numériques de cette collection sont valides et que le document n'a pas été falsifié, with Renvoie également`vrai` s'il n'y a pas de signatures numériques. `FAUX` si au moins une signature numérique est invalide.

```csharp
public bool IsValid { get; }
```

### Exemples

Montre comment signer des documents avec des certificats X.509.

```csharp
// Vérifiez qu'un document n'est pas signé.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Créez un objet CertificateHolder à partir d'un fichier PKCS12, que nous utiliserons pour signer le document.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Il existe deux manières d'enregistrer une copie signée d'un document dans le système de fichiers local :
// 1 - Désigne un document par un nom de fichier système local et enregistre une copie signée à un emplacement spécifié par un autre nom de fichier.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Extrayez un document d'un flux et enregistrez une copie signée dans un autre flux.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Veuillez vérifier que toutes les signatures numériques du document sont valides et vérifier leurs détails.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### Voir également

* class [DigitalSignatureCollection](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../digitalsignaturecollection/)
* Assemblée [Aspose.Words](../../../)


