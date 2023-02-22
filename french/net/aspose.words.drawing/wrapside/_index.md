---
title: Enum WrapSide
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Drawing.WrapSide énumération. Spécifie de quels côtés de la forme ou de limage le texte senroule autour.
type: docs
weight: 1240
url: /fr/net/aspose.words.drawing/wrapside/
---
## WrapSide enumeration

Spécifie de quel(s) côté(s) de la forme ou de l'image le texte s'enroule autour.

```csharp
public enum WrapSide
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Both | `0` | Le texte du document s'habille des deux côtés de la forme. |
| Left | `1` | Le texte du document s'habille uniquement sur le côté gauche de la forme. Il y a une zone de texte libre à droite de la forme. |
| Right | `2` | Le texte du document s'habille sur le côté droit de la forme uniquement. Il y a une zone de texte libre sur le côté gauche de la forme. |
| Largest | `3` | Le texte du document s'habille du côté de la forme le plus éloigné de la marge de la page, laissant une zone de texte libre de l'autre côté de la forme. |
| Default | `0` | La valeur par défaut estBoth . |

### Exemples

Montre comment remplacer toutes les formes de zone de texte par des formes d'image.

```csharp
Document doc = new Document(MyDir + "Textboxes in drawing canvas.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(3, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(1, shapes.Count(s => s.ShapeType == ShapeType.Image));

foreach (Shape shape in shapes)
{
    if (shape.ShapeType == ShapeType.TextBox)
    {
        Shape replacementShape = new Shape(doc, ShapeType.Image);
        replacementShape.ImageData.SetImage(ImageDir + "Logo.jpg");
        replacementShape.Left = shape.Left;
        replacementShape.Top = shape.Top;
        replacementShape.Width = shape.Width;
        replacementShape.Height = shape.Height;
        replacementShape.RelativeHorizontalPosition = shape.RelativeHorizontalPosition;
        replacementShape.RelativeVerticalPosition = shape.RelativeVerticalPosition;
        replacementShape.HorizontalAlignment = shape.HorizontalAlignment;
        replacementShape.VerticalAlignment = shape.VerticalAlignment;
        replacementShape.WrapType = shape.WrapType;
        replacementShape.WrapSide = shape.WrapSide;

        shape.ParentNode.InsertAfter(replacementShape, shape);
        shape.Remove();
    }
}

shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(0, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(4, shapes.Count(s => s.ShapeType == ShapeType.Image));

doc.Save(ArtifactsDir + "Shape.ReplaceTextboxesWithImages.docx");
```

### Voir également

* property [WrapSide](../shapebase/wrapside/)
* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)


