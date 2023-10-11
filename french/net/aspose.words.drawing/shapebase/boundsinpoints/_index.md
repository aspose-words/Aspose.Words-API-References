---
title: ShapeBase.BoundsInPoints
second_title: Référence de l'API Aspose.Words pour .NET
description: ShapeBase propriété. Obtient lemplacement et la taille du bloc contenant la forme en points par rapport à lancre de la forme la plus haute.
type: docs
weight: 80
url: /fr/net/aspose.words.drawing/shapebase/boundsinpoints/
---
## ShapeBase.BoundsInPoints property

Obtient l'emplacement et la taille du bloc contenant la forme en points, par rapport à l'ancre de la forme la plus haute.

```csharp
public RectangleF BoundsInPoints { get; }
```

### Exemples

Montre comment vérifier une forme contenant des limites de bloc.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Line, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 50, 100, 100, WrapType.None);
shape.StrokeColor = Color.Orange;

// Même si la ligne elle-même prend peu de place sur la page du document,
// il occupe un bloc contenant rectangulaire, dont nous pouvons déterminer la taille à l'aide des propriétés "Bounds".
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.Bounds);
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.BoundsInPoints);

// Créez une forme de groupe, puis définissez la taille de son bloc contenant à l'aide de la propriété "Bounds".
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(0, 100, 250, 250);

Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);

// Créez un rectangle, vérifiez la taille de son bloc de délimitation, puis ajoutez-le à la forme du groupe.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

Assert.AreEqual(new RectangleF(700, 700, 100, 100), shape.BoundsInPoints);

group.AppendChild(shape);

// Le plan de coordonnées de la forme de groupe a son origine dans le coin supérieur gauche de son bloc conteneur,
// et les coordonnées x et y de (1000, 1000) dans le coin inférieur droit.
// Notre forme de groupe mesure 250 x 250 pts, donc tous les 4 pts sur le plan de coordonnées de la forme de groupe.
// se traduit en 1 pt dans le plan de coordonnées du corps du document.
// Chaque forme que nous insérons verra également sa taille réduite d'un facteur 4.
// La modification de la propriété "BoundsInPoints" de la forme reflétera cela.
Assert.AreEqual(new RectangleF(175, 275, 25, 25), shape.BoundsInPoints);

doc.FirstSection.Body.FirstParagraph.AppendChild(group);

// Insère une forme et la place en dehors des limites du bloc contenant la forme de groupe.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 1000,
    Top = 1000
};

group.AppendChild(shape);

// L'empreinte de la forme de groupe dans le corps du document a augmenté, mais le bloc conteneur reste le même.
Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);
Assert.AreEqual(new RectangleF(250, 350, 25, 25), shape.BoundsInPoints);

doc.Save(ArtifactsDir + "Shape.Bounds.docx");
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../shapebase/)
* Assemblée [Aspose.Words](../../../)


