---
title: SignOptions.SignatureLineId
linktitle: SignatureLineId
articleTitle: SignatureLineId
second_title: Aspose.Words pour .NET
description: Découvrez la propriété SignatureLineId dans SignOptions. Identifiez facilement les lignes de signature grâce à un GUID unique, améliorant ainsi l'efficacité de votre gestion documentaire.
type: docs
weight: 50
url: /fr/net/aspose.words.digitalsignatures/signoptions/signaturelineid/
---
## SignOptions.SignatureLineId property

Identifiant de la ligne de signature. La valeur par défaut est**Guid vide (tous les zéros)** .

```csharp
public Guid SignatureLineId { get; set; }
```

## Remarques

Lorsqu'il est défini, il associe[`SignatureLine`](../../../aspose.words.drawing/signatureline/) avec correspondant[`DigitalSignature`](../../digitalsignature/) .

## Exemples

Montre comment ajouter une ligne de signature à un document, puis le signer à l'aide d'un certificat numérique.

```csharp
[Description("WORDSNET-16868")]
public static void Sign()
{
    string signeeName = "Ron Williams";
    string srcDocumentPath = MyDir + "Document.docx";
    string dstDocumentPath = ArtifactsDir + "SignDocumentCustom.Sign.docx";
    string certificatePath = MyDir + "morzal.pfx";
    string certificatePassword = "aw";

    CreateSignees();

    Signee signeeInfo = mSignees.Find(c => c.Name == signeeName);

    if (signeeInfo != null)
        SignDocument(srcDocumentPath, dstDocumentPath, signeeInfo, certificatePath, certificatePassword);
    else
        Assert.Fail("Signee does not exist.");
}

/// <summary>
/// Crée une copie d'un document source signé à l'aide des informations de signataire fournies et du certificat X509.
/// </summary>
private static void SignDocument(string srcDocumentPath, string dstDocumentPath,
    Signee signeeInfo, string certificatePath, string certificatePassword)
{
    Document document = new Document(srcDocumentPath);
    DocumentBuilder builder = new DocumentBuilder(document);

    // Configurer et insérer une ligne de signature, un objet dans le document qui affichera une signature avec laquelle nous le signerons.
    SignatureLineOptions signatureLineOptions = new SignatureLineOptions
    {
        Signer = signeeInfo.Name, 
        SignerTitle = signeeInfo.Position
    };

    SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
    signatureLine.Id = signeeInfo.PersonId;

    // Tout d’abord, nous allons enregistrer une version non signée de notre document.
    builder.Document.Save(dstDocumentPath);

    CertificateHolder certificateHolder = CertificateHolder.Create(certificatePath, certificatePassword);

    SignOptions signOptions = new SignOptions
    {
        SignatureLineId = signeeInfo.PersonId,
        SignatureLineImage = signeeInfo.Image
    };

    // Remplacez le document non signé que nous avons enregistré ci-dessus par une version signée à l'aide du certificat.
    DigitalSignatureUtil.Sign(dstDocumentPath, dstDocumentPath, certificateHolder, signOptions);
}

public class Signee
{
    public Guid PersonId { get; set; }
    public string Name { get; set; }
    public string Position { get; set; }
    public byte[] Image { get; set; }

    public Signee(Guid guid, string name, string position, byte[] image)
    {
        PersonId = guid;
        Name = name;
        Position = position;
        Image = image;
    }
}

private static void CreateSignees()
{
    var signImagePath = ImageDir + "Logo.jpg";

    mSignees = new List<Signee>
    {
        new Signee(Guid.NewGuid(), "Ron Williams", "Chief Executive Officer", TestUtil.ImageToByteArray(signImagePath)),
        new Signee(Guid.NewGuid(), "Stephen Morse", "Head of Compliance", TestUtil.ImageToByteArray(signImagePath))
    };
}

private static List<Signee> mSignees;
```

### Voir également

* class [SignOptions](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Assemblée [Aspose.Words](../../../)
