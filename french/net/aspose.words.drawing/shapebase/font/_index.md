---
title: ShapeBase.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words pour .NET
description: ShapeBase Font propriété. Donne accès au formatage de la police de cet objet en C#.
type: docs
weight: 190
url: /fr/net/aspose.words.drawing/shapebase/font/
---
## ShapeBase.Font property

Donne accès au formatage de la police de cet objet.

```csharp
public Font Font { get; }
```

## Exemples

Montre comment insérer une zone de texte et définir la police de son contenu.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.TextBox, 300, 50);
builder.MoveTo(shape.LastParagraph);
builder.Write("This text is inside the text box.");

// Définissez la propriété "Caché" de l'objet "Font" de la forme sur "true" pour masquer la zone de texte à la vue
// et réduit l'espace qu'il occuperait normalement.
// Définissez la propriété "Caché" de l'objet "Font" de la forme sur "false" pour laisser la zone de texte visible.
shape.Font.Hidden = hideShape;

// Si la forme est visible, nous modifierons son apparence via l'objet font.
if (!hideShape)
{
    shape.Font.HighlightColor = Color.LightGray;
    shape.Font.Color = Color.Red;
    shape.Font.Underline = Underline.Dash;
}

// Déplace le générateur hors de la zone de texte vers le document principal.
builder.MoveTo(shape.ParentParagraph);

builder.Writeln("\nThis text is outside the text box.");

doc.Save(ArtifactsDir + "Shape.Font.docx");
```

### Voir également

* class [Font](../../../aspose.words/font/)
* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
