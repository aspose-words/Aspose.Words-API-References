---
title: DigitalSignature.SubjectName
linktitle: SubjectName
articleTitle: SubjectName
second_title: Aspose.Words pour .NET
description: Découvrez la propriété DigitalSignature SubjectName, qui révèle le nom distinctif du sujet du certificat, améliorant ainsi l'authenticité et la sécurité du document.
type: docs
weight: 80
url: /fr/net/aspose.words.digitalsignatures/digitalsignature/subjectname/
---
## DigitalSignature.SubjectName property

Renvoie le nom distinctif du sujet du certificat qui a été utilisé pour signer le document.

```csharp
public string SubjectName { get; }
```

## Exemples

Montre comment signer des documents avec des certificats X.509.

```csharp
// Vérifier qu'un document n'est pas signé.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Créez un objet CertificateHolder à partir d'un fichier PKCS12, que nous utiliserons pour signer le document.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Il existe deux manières d'enregistrer une copie signée d'un document sur le système de fichiers local :
// 1 - Désignez un document par un nom de fichier système local et enregistrez une copie signée à un emplacement spécifié par un autre nom de fichier.
SignOptions signOptions = new SignOptions { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx",
    certificateHolder, signOptions);

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Prendre un document d'un flux et enregistrer une copie signée dans un autre flux.
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

* class [DigitalSignature](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Assemblée [Aspose.Words](../../../)
