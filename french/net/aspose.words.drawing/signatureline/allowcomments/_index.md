---
title: SignatureLine.AllowComments
linktitle: AllowComments
articleTitle: AllowComments
second_title: Aspose.Words pour .NET
description: Découvrez la propriété SignatureLine AllowComments, qui permet aux signataires d'ajouter des commentaires dans la boîte de dialogue Signature pour un retour amélioré. La valeur par défaut est « false ».
type: docs
weight: 10
url: /fr/net/aspose.words.drawing/signatureline/allowcomments/
---
## SignatureLine.AllowComments property

Obtient ou définit une valeur indiquant que le signataire peut ajouter des commentaires dans la boîte de dialogue Signature. La valeur par défaut de cette propriété est`FAUX` .

```csharp
public bool AllowComments { get; set; }
```

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

// Insérer une forme qui contiendra une ligne de signature, dont nous allons
// personnaliser en utilisant l'objet "SignatureLineOptions" que nous avons créé ci-dessus.
// Si nous insérons une forme dont les coordonnées proviennent du coin inférieur droit de la page,
// nous devrons fournir des coordonnées x et y négatives pour mettre la forme en vue.
Shape shape = builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, -170.0,
        RelativeVerticalPosition.BottomMargin, -60.0, WrapType.None);

Assert.True(shape.IsSignatureLine);

// Vérifiez les propriétés de notre ligne de signature via son objet Shape.
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

* class [SignatureLine](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
