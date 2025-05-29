---
title: ShapeBase.DistanceTop
linktitle: DistanceTop
articleTitle: DistanceTop
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShapeBase DistanceTop, ajustez facilement l'espace en points entre le texte de votre document et le bord supérieur de la forme pour un contrôle précis de la mise en page.
type: docs
weight: 160
url: /fr/net/aspose.words.drawing/shapebase/distancetop/
---
## ShapeBase.DistanceTop property

Renvoie ou définit la distance (en points) entre le texte du document et le bord supérieur de la forme.

```csharp
public double DistanceTop { get; set; }
```

## Remarques

La valeur par défaut est 0.

N'a d'effet que sur les formes de niveau supérieur.

## Exemples

Montre comment définir la distance d'habillage d'un texte qui entoure une forme.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérez un rectangle et faites en sorte que le texte s'enroule étroitement autour de ses limites.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 150, 150);
shape.WrapType = WrapType.Tight;

// Définissez la distance minimale entre la forme et le texte environnant à 40 pt de tous les côtés.
shape.DistanceTop = 40;
shape.DistanceBottom = 40;
shape.DistanceLeft = 40;
shape.DistanceRight = 40;

// Déplacez la forme plus près du centre de la page, puis faites pivoter la forme de 60 degrés dans le sens des aiguilles d'une montre.
shape.Top = 75;
shape.Left = 150;
shape.Rotation = 60;

// Ajoutez du texte qui s'enroulera autour de la forme.
builder.Font.Size = 24;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "Shape.Coordinates.docx");
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
