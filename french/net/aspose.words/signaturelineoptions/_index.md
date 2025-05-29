---
title: SignatureLineOptions Class
linktitle: SignatureLineOptions
articleTitle: SignatureLineOptions
second_title: Aspose.Words pour .NET
description: Découvrez Aspose.Words.SignatureLineOptions pour personnaliser facilement les lignes de signature de vos documents. Améliorez votre expérience DocumentBuilder dès aujourd'hui !
type: docs
weight: 6940
url: /fr/net/aspose.words/signaturelineoptions/
---
## SignatureLineOptions class

Permet de spécifier les options d'insertion de la ligne de signature. Utilisé dans[`DocumentBuilder`](../documentbuilder/) .

Pour en savoir plus, visitez le[Travailler avec des signatures numériques](https://docs.aspose.com/words/net/working-with-digital-signatures/) article de documentation.

```csharp
public class SignatureLineOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [SignatureLineOptions](signaturelineoptions/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [AllowComments](../../aspose.words/signaturelineoptions/allowcomments/) { get; set; } | Obtient ou définit une valeur indiquant que le signataire peut ajouter des commentaires dans la boîte de dialogue Signature. La valeur par défaut de cette propriété est`FAUX` . |
| [DefaultInstructions](../../aspose.words/signaturelineoptions/defaultinstructions/) { get; set; } | Obtient ou définit une valeur indiquant que les instructions par défaut sont affichées dans la boîte de dialogue Signature. La valeur par défaut de cette propriété est`vrai` . |
| [Email](../../aspose.words/signaturelineoptions/email/) { get; set; } | Obtient ou définit l'adresse e-mail suggérée du signataire. La valeur par défaut de cette propriété est**chaîne vide** (Empty ). |
| [Instructions](../../aspose.words/signaturelineoptions/instructions/) { get; set; } | Obtient ou définit les instructions au signataire qui sont affichées lors de la signature de la ligne de signature. La valeur par défaut de cette propriété est**chaîne vide** (Empty ). |
| [ShowDate](../../aspose.words/signaturelineoptions/showdate/) { get; set; } | Obtient ou définit une valeur indiquant que la date de signature est affichée dans la ligne de signature. La valeur par défaut de cette propriété est`vrai` . |
| [Signer](../../aspose.words/signaturelineoptions/signer/) { get; set; } | Obtient ou définit le signataire suggéré de la ligne de signature. La valeur par défaut de cette propriété est**chaîne vide** (Empty ). |
| [SignerTitle](../../aspose.words/signaturelineoptions/signertitle/) { get; set; } | Obtient ou définit le titre suggéré du signataire. La valeur par défaut de cette propriété est**chaîne vide** (Empty ). |

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

// Rouvrez notre document enregistré et vérifiez que les propriétés « IsSigned » et « IsValid » sont toutes deux égales à « true »,
// indiquant que la ligne de signature contient une signature.
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
