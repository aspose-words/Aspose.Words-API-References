---
title: ShapeBase.Fill
second_title: Référence de l'API Aspose.Words pour .NET
description: ShapeBase propriété. Obtient la mise en forme de remplissage pour la forme.
type: docs
weight: 170
url: /fr/net/aspose.words.drawing/shapebase/fill/
---
## ShapeBase.Fill property

Obtient la mise en forme de remplissage pour la forme.

```csharp
public Fill Fill { get; }
```

### Exemples

Montre comment remplir une forme avec une couleur unie.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Écrivez du texte, puis recouvrez-le d'une forme flottante.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Utilisez la propriété "StrokeColor" pour définir la couleur du contour de la forme.
shape.StrokeColor = Color.CadetBlue;

// Utilisez la propriété "FillColor" pour définir la couleur de la zone intérieure de la forme.
shape.FillColor = Color.LightBlue;

// La propriété "Opacité" détermine la transparence de la couleur sur une échelle de 0 à 1,
// avec 1 étant entièrement opaque et 0 étant invisible.
// Le remplissage de la forme par défaut est entièrement opaque, nous ne pouvons donc pas voir le texte sur lequel cette forme se trouve.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Définit l'opacité de la couleur de remplissage de la forme sur une valeur inférieure afin que nous puissions voir le texte en dessous.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Voir également

* class [Fill](../../fill/)
* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../shapebase/)
* Assemblée [Aspose.Words](../../../)


