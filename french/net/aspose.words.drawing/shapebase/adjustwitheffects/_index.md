---
title: ShapeBase.AdjustWithEffects
linktitle: AdjustWithEffects
articleTitle: AdjustWithEffects
second_title: Aspose.Words pour .NET
description: ShapeBase AdjustWithEffects méthode. Ajoute au rectangle source les valeurs de létendue de leffet et renvoie le rectangle final en C#.
type: docs
weight: 620
url: /fr/net/aspose.words.drawing/shapebase/adjustwitheffects/
---
## ShapeBase.AdjustWithEffects method

Ajoute au rectangle source les valeurs de l'étendue de l'effet et renvoie le rectangle final.

```csharp
public RectangleF AdjustWithEffects(RectangleF source)
```

## Exemples

Montre comment vérifier comment les limites d’une forme sont affectées par les effets de forme.

```csharp
Document doc = new Document(MyDir + "Shape shadow effect.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

// Les deux formes sont identiques en termes de dimensions et de type de forme.
Assert.AreEqual(shapes[0].Width, shapes[1].Width);
Assert.AreEqual(shapes[0].Height, shapes[1].Height);
Assert.AreEqual(shapes[0].ShapeType, shapes[1].ShapeType);

// La première forme n'a aucun effet et la seconde a une ombre et un contour épais.
// Ces effets rendent la taille de la silhouette de la deuxième forme plus grande que celle de la première.
// Même si la taille du rectangle apparaît lorsqu'on clique sur ces formes dans Microsoft Word,
// les limites extérieures visibles de la deuxième forme sont affectées par l'ombre et le contour et sont donc plus grandes.
// Nous pouvons utiliser la méthode "AdjustWithEffects" pour voir la vraie taille de la forme.
Assert.AreEqual(0.0, shapes[0].StrokeWeight);
Assert.AreEqual(20.0, shapes[1].StrokeWeight);
Assert.False(shapes[0].ShadowEnabled);
Assert.True(shapes[1].ShadowEnabled);

Shape shape = shapes[0];

// Crée un objet RectangleF, représentant un rectangle,
// que nous pourrions potentiellement utiliser comme coordonnées et limites d'une forme.
RectangleF rectangleF = new RectangleF(200, 200, 1000, 1000);

// Exécutez cette méthode pour ajuster la taille du rectangle pour tous nos effets de forme.
RectangleF rectangleFOut = shape.AdjustWithEffects(rectangleF);

// Puisque la forme n'a aucun effet de changement de bordure, ses dimensions de bordure ne sont pas affectées.
Assert.AreEqual(200, rectangleFOut.X);
Assert.AreEqual(200, rectangleFOut.Y);
Assert.AreEqual(1000, rectangleFOut.Width);
Assert.AreEqual(1000, rectangleFOut.Height);

// Vérifiez l'étendue finale de la première forme, en points.
Assert.AreEqual(0, shape.BoundsWithEffects.X);
Assert.AreEqual(0, shape.BoundsWithEffects.Y);
Assert.AreEqual(147, shape.BoundsWithEffects.Width);
Assert.AreEqual(147, shape.BoundsWithEffects.Height);

shape = shapes[1];
rectangleF = new RectangleF(200, 200, 1000, 1000);
rectangleFOut = shape.AdjustWithEffects(rectangleF);

// Les effets de forme ont légèrement déplacé le coin supérieur gauche apparent de la forme.
Assert.AreEqual(171.5, rectangleFOut.X);
Assert.AreEqual(167, rectangleFOut.Y);

// Les effets ont également affecté les dimensions visibles de la forme.
Assert.AreEqual(1045, rectangleFOut.Width);
Assert.AreEqual(1132, rectangleFOut.Height);

// Les effets ont également affecté les limites visibles de la forme.
Assert.AreEqual(-28.5, shape.BoundsWithEffects.X);
Assert.AreEqual(-33, shape.BoundsWithEffects.Y);
Assert.AreEqual(192, shape.BoundsWithEffects.Width);
Assert.AreEqual(279, shape.BoundsWithEffects.Height);
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
