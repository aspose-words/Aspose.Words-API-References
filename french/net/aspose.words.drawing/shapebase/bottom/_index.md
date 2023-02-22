---
title: ShapeBase.Bottom
second_title: Référence de l'API Aspose.Words pour .NET
description: ShapeBase propriété. Obtient la position du bord inférieur du bloc conteneur de la forme.
type: docs
weight: 60
url: /fr/net/aspose.words.drawing/shapebase/bottom/
---
## ShapeBase.Bottom property

Obtient la position du bord inférieur du bloc conteneur de la forme.

```csharp
public double Bottom { get; }
```

### Remarques

Pour une forme de niveau supérieur, la valeur est exprimée en points et relative à l'ancre de la forme.

Pour les formes d'un groupe, la valeur est dans l'espace de coordonnées et les unités du groupe parent.

### Exemples

Montre comment insérer une image flottante et spécifier sa position et sa taille.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Configure la propriété "RelativeHorizontalPosition" de la forme pour traiter la valeur de la propriété "Left"
 // comme la distance horizontale de la forme, en points, depuis le côté gauche de la page.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Définit la distance horizontale de la forme depuis le côté gauche de la page sur 100.
shape.Left = 100;

// Utilisez la propriété "RelativeVerticalPosition" de la même manière pour positionner la forme 80 pt sous le haut de la page.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Définit la hauteur de la forme, qui redimensionnera automatiquement la largeur pour conserver les dimensions.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// Les propriétés "Bottom" et "Right" contiennent les bords bas et droit de l'image.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../shapebase/)
* Assemblée [Aspose.Words](../../../)


