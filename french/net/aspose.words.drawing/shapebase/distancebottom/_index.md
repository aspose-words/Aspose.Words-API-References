---
title: ShapeBase.DistanceBottom
linktitle: DistanceBottom
articleTitle: DistanceBottom
second_title: Aspose.Words pour .NET
description: ShapeBase DistanceBottom propriété. Renvoie ou définit la distance en points entre le texte du document et le bord inférieur de la forme en C#.
type: docs
weight: 130
url: /fr/net/aspose.words.drawing/shapebase/distancebottom/
---
## ShapeBase.DistanceBottom property

Renvoie ou définit la distance (en points) entre le texte du document et le bord inférieur de la forme.

```csharp
public double DistanceBottom { get; set; }
```

## Remarques

La valeur par défaut est 0.

N'a d'effet que sur les formes de niveau supérieur.

## Exemples

Montre comment définir la distance d’habillage d’un texte entourant une forme.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère un rectangle et enroule le texte étroitement autour de ses limites.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 150, 150);
shape.WrapType = WrapType.Tight;

// Définit la distance minimale entre la forme et le texte environnant à 40 points de tous les côtés.
shape.DistanceTop = 40;
shape.DistanceBottom = 40;
shape.DistanceLeft = 40;
shape.DistanceRight = 40;

// Rapprochez la forme du centre de la page, puis faites-la pivoter de 60 degrés dans le sens des aiguilles d'une montre.
shape.Top = 75;
shape.Left = 150; 
shape.Rotation = 60;

// Ajoute du texte qui entourera la forme.
builder.Font.Size = 24;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "Shape.Coordinates.docx");
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
