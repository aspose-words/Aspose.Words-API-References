---
title: SignatureLine Class
linktitle: SignatureLine
articleTitle: SignatureLine
second_title: Aspose.Words pour .NET
description: Aspose.Words.Drawing.SignatureLine classe. Donne accès aux propriétés de la ligne de signature en C#.
type: docs
weight: 1300
url: /fr/net/aspose.words.drawing/signatureline/
---
## SignatureLine class

Donne accès aux propriétés de la ligne de signature.

Pour en savoir plus, visitez le[Travailler avec des signatures numériques](https://docs.aspose.com/words/net/working-with-digital-signatures/) article documentaire.

```csharp
public class SignatureLine
```

## Propriétés

| Nom | La description |
| --- | --- |
| [AllowComments](../../aspose.words.drawing/signatureline/allowcomments/) { get; set; } | Obtient ou définit une valeur indiquant que le signataire peut ajouter des commentaires dans la boîte de dialogue Signer. La valeur par défaut de cette propriété est`FAUX` . |
| [DefaultInstructions](../../aspose.words.drawing/signatureline/defaultinstructions/) { get; set; } | Obtient ou définit une valeur indiquant que les instructions par défaut sont affichées dans la boîte de dialogue de signature. La valeur par défaut de cette propriété est`vrai` . |
| [Email](../../aspose.words.drawing/signatureline/email/) { get; set; } | Obtient ou définit l'adresse e-mail du signataire suggéré. La valeur par défaut de cette propriété est**chaîne vide** (Empty). |
| [Id](../../aspose.words.drawing/signatureline/id/) { get; set; } | Obtient ou définit l'identifiant de cette ligne de signature. |
| [Instructions](../../aspose.words.drawing/signatureline/instructions/) { get; set; } | Obtient ou définit les instructions destinées au signataire qui sont affichées lors de la signature de la ligne de signature. Cette propriété est ignorée si[`DefaultInstructions`](./defaultinstructions/)est défini. La valeur par défaut de cette propriété est**chaîne vide** (Empty). |
| [IsSigned](../../aspose.words.drawing/signatureline/issigned/) { get; } | Indique que la ligne de signature est signée par signature numérique. |
| [IsValid](../../aspose.words.drawing/signatureline/isvalid/) { get; } | Indique que la ligne de signature est signée par signature numérique et que cette signature numérique est valide. |
| [ProviderId](../../aspose.words.drawing/signatureline/providerid/) { get; set; } | Obtient ou définit l'identifiant du fournisseur de signature pour cette ligne de signature. La valeur par défaut est "{00000000-0000-0000-0000-000000000000}". |
| [ShowDate](../../aspose.words.drawing/signatureline/showdate/) { get; set; } | Obtient ou définit une valeur indiquant que la date de signature est affichée dans la ligne de signature. La valeur par défaut de cette propriété est`vrai` . |
| [Signer](../../aspose.words.drawing/signatureline/signer/) { get; set; } | Obtient ou définit le signataire suggéré de la ligne de signature. La valeur par défaut de cette propriété est**chaîne vide** (Empty). |
| [SignerTitle](../../aspose.words.drawing/signatureline/signertitle/) { get; set; } | Obtient ou définit le titre suggéré du signataire (par exemple, Manager). La valeur par défaut de cette propriété est**chaîne vide** (Empty). |

## Exemples

Montre comment créer une ligne pour une signature et l'insérer dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions options = new SignatureLineOptions
{
    AllowComments = true,
    DefaultInstructions = true,
    Email = "john.doe@management.com",
    Instructions = "Please sign here",
    ShowDate = true,
    Signer = "John Doe",
    SignerTitle = "Senior Manager"
};

// Insère une forme qui contiendra une ligne de signature, dont nous allons
// personnalisez à l'aide de l'objet "SignatureLineOptions" que nous avons créé ci-dessus.
// Si on insère une forme dont les coordonnées proviennent du coin inférieur droit de la page,
// nous devrons fournir des coordonnées x et y négatives pour faire apparaître la forme.
Shape shape = builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, -170.0, 
        RelativeVerticalPosition.BottomMargin, -60.0, WrapType.None);

Assert.True(shape.IsSignatureLine);

// Vérifier les propriétés de notre ligne de signature via son objet Shape.
SignatureLine signatureLine = shape.SignatureLine;

Assert.AreEqual("john.doe@management.com", signatureLine.Email);
Assert.AreEqual("John Doe", signatureLine.Signer);
Assert.AreEqual("Senior Manager", signatureLine.SignerTitle);
Assert.AreEqual("Please sign here", signatureLine.Instructions);
Assert.True(signatureLine.ShowDate);
Assert.True(signatureLine.AllowComments);
Assert.True(signatureLine.DefaultInstructions);

doc.Save(ArtifactsDir + "Shape.SignatureLine.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
