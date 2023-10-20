---
title: ShapeBase.Top
linktitle: Top
articleTitle: Top
second_title: Aspose.Words pour .NET
description: ShapeBase Top propriété. Obtient ou définit la position du bord supérieur du bloc contenant la forme en C#.
type: docs
weight: 540
url: /fr/net/aspose.words.drawing/shapebase/top/
---
## ShapeBase.Top property

Obtient ou définit la position du bord supérieur du bloc contenant la forme.

```csharp
public double Top { get; set; }
```

## Remarques

Pour une forme de niveau supérieur, la valeur est en points et par rapport à l'ancre de la forme.

Pour les formes d'un groupe, la valeur se trouve dans l'espace de coordonnées et les unités du groupe parent.

La valeur par défaut est 0.

N'a d'effet que sur les formes flottantes.

## Exemples

Montre comment insérer une image flottante et spécifier sa position et sa taille.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Configure la propriété "RelativeHorizontalPosition" de la forme pour traiter la valeur de la propriété "Left"
 // comme distance horizontale de la forme, en points, depuis le côté gauche de la page.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Définit la distance horizontale de la forme depuis le côté gauche de la page sur 100.
shape.Left = 100;

// Utilisez la propriété "RelativeVerticalPosition" de la même manière pour positionner la forme 80 pt en dessous du haut de la page.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Définit la hauteur de la forme, qui mettra automatiquement à l'échelle la largeur pour préserver les dimensions.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// Les propriétés "Bottom" et "Right" contiennent les bords inférieur et droit de l'image.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
