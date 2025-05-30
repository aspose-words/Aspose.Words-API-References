---
title: ShapeBase.ParentParagraph
linktitle: ParentParagraph
articleTitle: ParentParagraph
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShapeBase ParentParagraph  accédez efficacement au paragraphe parent immédiat pour une gestion de contenu simplifiée et une organisation améliorée.
type: docs
weight: 430
url: /fr/net/aspose.words.drawing/shapebase/parentparagraph/
---
## ShapeBase.ParentParagraph property

Renvoie le paragraphe parent immédiat.

```csharp
public Paragraph ParentParagraph { get; }
```

## Remarques

Pour les formes enfants d'une forme de groupe et les formes enfants d'un objet Office Math, renvoie toujours`nul`.

## Exemples

Montre comment insérer une zone de texte et définir la police de son contenu.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.TextBox, 300, 50);
builder.MoveTo(shape.LastParagraph);
builder.Write("This text is inside the text box.");

// Définissez la propriété « Hidden » de l'objet « Font » de la forme sur « true » pour masquer la zone de texte
// et réduire l'espace qu'il occuperait normalement.
// Définissez la propriété « Hidden » de l'objet « Font » de la forme sur « false » pour laisser la zone de texte visible.
shape.Font.Hidden = hideShape;

// Si la forme est visible, nous modifierons son apparence via l'objet police.
if (!hideShape)
{
    shape.Font.HighlightColor = Color.LightGray;
    shape.Font.Color = Color.Red;
    shape.Font.Underline = Underline.Dash;
}

// Déplacez le générateur hors de la zone de texte vers le document principal.
builder.MoveTo(shape.ParentParagraph);

builder.Writeln("\nThis text is outside the text box.");

doc.Save(ArtifactsDir + "Shape.Font.docx");
```

### Voir également

* class [Paragraph](../../../aspose.words/paragraph/)
* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
