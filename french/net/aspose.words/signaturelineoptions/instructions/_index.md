---
title: SignatureLineOptions.Instructions
second_title: Référence de l'API Aspose.Words pour .NET
description: SignatureLineOptions propriété. Obtient ou définit les instructions destinées au signataire qui sont affichées lors de la signature de la ligne de signature. La valeur par défaut de cette propriété est chaîne vide Empty.
type: docs
weight: 50
url: /fr/net/aspose.words/signaturelineoptions/instructions/
---
## SignatureLineOptions.Instructions property

Obtient ou définit les instructions destinées au signataire qui sont affichées lors de la signature de la ligne de signature. La valeur par défaut de cette propriété est **chaîne vide** (Empty).

```csharp
public string Instructions { get; set; }
```

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

// Rouvrez notre document enregistré et vérifiez que les propriétés "IsSigned" et "IsValid" sont toutes deux égales à "true",
// indiquant que la ligne de signature contient une signature.
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### Voir également

* class [SignatureLineOptions](../)
* espace de noms [Aspose.Words](../../signaturelineoptions/)
* Assemblée [Aspose.Words](../../../)


