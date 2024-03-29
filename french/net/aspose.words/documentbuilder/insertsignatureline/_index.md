---
title: DocumentBuilder.InsertSignatureLine
linktitle: InsertSignatureLine
articleTitle: InsertSignatureLine
second_title: Aspose.Words pour .NET
description: DocumentBuilder InsertSignatureLine méthode. Insère une ligne de signature à la position actuelle en C#.
type: docs
weight: 440
url: /fr/net/aspose.words/documentbuilder/insertsignatureline/
---
## InsertSignatureLine(*[SignatureLineOptions](../../signaturelineoptions/)*) {#insertsignatureline}

Insère une ligne de signature à la position actuelle.

```csharp
public Shape InsertSignatureLine(SignatureLineOptions signatureLineOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| signatureLineOptions | SignatureLineOptions | L'objet qui stocke les paramètres de création de la ligne de signature. |

### Return_Value

Le nœud de ligne de signature qui vient d'être inséré.

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

* class [Shape](../../../aspose.words.drawing/shape/)
* class [SignatureLineOptions](../../signaturelineoptions/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## InsertSignatureLine(*[SignatureLineOptions](../../signaturelineoptions/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertsignatureline_1}

Insère une ligne de signature à la position spécifiée.

```csharp
public Shape InsertSignatureLine(SignatureLineOptions signatureLineOptions, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    WrapType wrapType)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| signatureLineOptions | SignatureLineOptions | L'objet qui stocke les paramètres de création de la ligne de signature. |
| horzPos | RelativeHorizontalPosition | Spécifie l'endroit à partir duquel la distance jusqu'à la ligne de signature est mesurée. |
| left | Double | Distance en points depuis l'origine jusqu'au côté gauche de la ligne de signature. |
| vertPos | RelativeVerticalPosition | Spécifie l'endroit à partir duquel la distance jusqu'à la ligne de signature est mesurée. |
| top | Double | Distance en points depuis l'origine jusqu'au côté supérieur de la ligne de signature. |
| wrapType | WrapType | Spécifie comment enrouler le texte autour de la ligne de signature. |

### Return_Value

Le nœud de ligne de signature qui vient d'être inséré.

## Remarques

Vous pouvez modifier la taille de l'image, l'emplacement, la méthode de positionnement et d'autres paramètres à l'aide du [`Shape`](../../../aspose.words.drawing/shape/) objet renvoyé par cette méthode.

## Exemples

Montre comment insérer une ligne de signature en ligne dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions options = new SignatureLineOptions
{
    Signer = "John Doe",
    SignerTitle = "Manager",
    Email = "johndoe@aspose.com",
    ShowDate = true,
    DefaultInstructions = false,
    Instructions = "Please sign here.",
    AllowComments = true
};

builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, 2.0,
    RelativeVerticalPosition.Page, 3.0, WrapType.Inline);

// La ligne de signature peut être signée dans Microsoft Word en double-cliquant dessus.
doc.Save(ArtifactsDir + "DocumentBuilder.SignatureLineInline.docx");
```

### Voir également

* class [Shape](../../../aspose.words.drawing/shape/)
* class [SignatureLineOptions](../../signaturelineoptions/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
