---
title: SignOptions.ProviderId
linktitle: ProviderId
articleTitle: ProviderId
second_title: Aspose.Words pour .NET
description: SignOptions ProviderId propriété. Spécifie lID de classe du fournisseur de signature. La valeur par défaut estGuide vide tous les zéros  en C#.
type: docs
weight: 40
url: /fr/net/aspose.words.digitalsignatures/signoptions/providerid/
---
## SignOptions.ProviderId property

Spécifie l'ID de classe du fournisseur de signature. La valeur par défaut est**Guide vide (tous les zéros)** .

```csharp
public Guid ProviderId { get; set; }
```

## Remarques

Le fournisseur de services cryptographiques (CSP) est un module logiciel indépendant qui exécute réellement des algorithmes de cryptographie pour l'authentification, le codage et le cryptage. MS Office réserve la valeur de {00000000-0000-0000-0000-000000000000} pour son fournisseur de signature par défaut.

Le GUID du fournisseur supplémentaire installé doit être obtenu à partir de la documentation livrée avec le fournisseur.

De plus, tous les fournisseurs cryptographiques installés sont répertoriés dans le registre Windows. On le trouve dans le chemin suivant : HKLM\SOFTWARE\Microsoft\Cryptography\Defaults\Provider. Il existe un nom de clé « CP Service UUID » qui correspond à un GUID du fournisseur de signature.

## Exemples

Montre comment signer un document avec un certificat personnel et une ligne de signature.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions signatureLineOptions = new SignatureLineOptions
{
    Signer = "vderyushev",
    SignerTitle = "QA",
    Email = "vderyushev@aspose.com",
    ShowDate = true,
    DefaultInstructions = false,
    Instructions = "Please sign here.",
    AllowComments = true
};

SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
signatureLine.ProviderId = Guid.Parse("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2");

Assert.False(signatureLine.IsSigned);
Assert.False(signatureLine.IsValid);

doc.Save(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.docx");

SignOptions signOptions = new SignOptions
{
    SignatureLineId = signatureLine.Id,
    ProviderId = signatureLine.ProviderId,
    Comments = "Document was signed by vderyushev",
    SignTime = DateTime.Now
};

CertificateHolder certHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

DigitalSignatureUtil.Sign(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.docx", 
    ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

// Rouvrez notre document enregistré et vérifiez que les propriétés "IsSigned" et "IsValid" sont toutes deux égales à "true",
// indiquant que la ligne de signature contient une signature.
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### Voir également

* class [SignOptions](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Assemblée [Aspose.Words](../../../)
