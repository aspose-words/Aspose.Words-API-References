---
title: Document.DigitalSignatures
linktitle: DigitalSignatures
articleTitle: DigitalSignatures
second_title: Aspose.Words pour .NET
description: Document DigitalSignatures propriété. Obtient la collection de signatures numériques pour ce document et leurs résultats de validation en C#.
type: docs
weight: 100
url: /fr/net/aspose.words/document/digitalsignatures/
---
## Document.DigitalSignatures property

Obtient la collection de signatures numériques pour ce document et leurs résultats de validation.

```csharp
public DigitalSignatureCollection DigitalSignatures { get; }
```

## Remarques

Cette collection contient des signatures numériques chargées à partir du document original. Ces signatures numériques ne seront pas enregistrées lorsque vous enregistrerez ce document.[`Document`](../) object dans un fichier ou un flux car l'enregistrement ou la conversion produira un document différent de l'original et les signatures numériques originales ne seront plus valides.

Cette collection n'est jamais`nul`. Si le document n'est pas signé, il ne contiendra aucun élément.

## Exemples

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

* class [DigitalSignatureCollection](../../../aspose.words.digitalsignatures/digitalsignaturecollection/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
