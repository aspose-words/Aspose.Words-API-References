---
title: SignatureLine.ProviderId
second_title: Référence de l'API Aspose.Words pour .NET
description: SignatureLine propriété. Obtient ou définit lidentifiant du fournisseur de signature pour cette ligne de signature. La valeur par défaut est 00000000000000000000000000000000.
type: docs
weight: 80
url: /fr/net/aspose.words.drawing/signatureline/providerid/
---
## SignatureLine.ProviderId property

Obtient ou définit l'identifiant du fournisseur de signature pour cette ligne de signature. La valeur par défaut est "{00000000-0000-0000-0000-000000000000}".

```csharp
public Guid ProviderId { get; set; }
```

### Remarques

Le fournisseur de services cryptographiques (CSP) est un module logiciel indépendant qui exécute en fait des algorithmes de cryptographie pour l'authentification, le codage et le cryptage. MS Office réserve la valeur de {00000000-0000-0000-0000-000000000000} pour son fournisseur de signature par défaut.

Le GUID du fournisseur installé en plus doit être obtenu à partir de la documentation fournie avec le fournisseur.

De plus, tous les fournisseurs de chiffrement installés sont énumérés dans le registre Windows. Il se trouve dans le chemin suivant : HKLM\SOFTWARE\Microsoft\Cryptography\Defaults\Provider. Il existe un nom de clé "CP Service UUID" qui correspond à un GUID de fournisseur de signature.

### Exemples

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

// Rouvrez notre document enregistré et vérifiez que les propriétés "IsSigned" et "IsValid" sont toutes les deux égales à "true",
// indiquant que la ligne de signature contient une signature.
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### Voir également

* class [SignatureLine](../)
* espace de noms [Aspose.Words.Drawing](../../signatureline/)
* Assemblée [Aspose.Words](../../../)


