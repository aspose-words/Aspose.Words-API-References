---
title: ShapeBase.Right
linktitle: Right
articleTitle: Right
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShapeBase Right pour accéder facilement à la position du bord droit du bloc contenant votre forme pour un contrôle précis de la mise en page.
type: docs
weight: 490
url: /fr/net/aspose.words.drawing/shapebase/right/
---
## ShapeBase.Right property

Obtient la position du bord droit du bloc contenant la forme.

```csharp
public double Right { get; }
```

## Remarques

Pour une forme de niveau supérieur, la valeur est en points et relative à l'ancre de forme.

Pour les formes d'un groupe, la valeur est dans l'espace de coordonnées et les unités du groupe parent.

## Exemples

Montre comment insérer une image flottante et spécifier sa position et sa taille.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Configurez la propriété « RelativeHorizontalPosition » de la forme pour traiter la valeur de la propriété « Left »
 // comme la distance horizontale de la forme, en points, à partir du côté gauche de la page.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Définissez la distance horizontale de la forme par rapport au côté gauche de la page sur 100.
shape.Left = 100;

// Utilisez la propriété « RelativeVerticalPosition » de manière similaire pour positionner la forme 80 pt sous le haut de la page.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Définissez la hauteur de la forme, ce qui mettra automatiquement à l'échelle la largeur pour préserver les dimensions.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// Les propriétés « Bottom » et « Right » contiennent les bords inférieur et droit de l'image.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
