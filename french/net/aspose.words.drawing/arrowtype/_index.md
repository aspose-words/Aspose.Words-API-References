---
title: ArrowType Enum
linktitle: ArrowType
articleTitle: ArrowType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Drawing.ArrowType pour personnaliser les styles de flèches pour les fins de ligne, améliorant ainsi l'attrait visuel et la précision de votre document.
type: docs
weight: 730
url: /fr/net/aspose.words.drawing/arrowtype/
---
## ArrowType enumeration

Spécifie le type d'une flèche à la fin d'une ligne.

```csharp
public enum ArrowType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | La ligne n'a pas de flèche à la fin. |
| Arrow | `1` | La flèche est un triangle plein. |
| Stealth | `2` | La flèche est une flèche « furtive ». |
| Diamond | `3` | L'extrémité de la ligne est un diamant solide. |
| Oval | `4` | L'extrémité de la ligne est un ovale plein. |
| Open | `5` | La flèche est une flèche ouverte. |
| Default | `0` | Identique àNone . |

## Exemples

Montre comment créer une variété de formes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous quatre exemples de formes que nous pouvons insérer dans nos documents.
// 1 - Ligne rouge pointillée horizontale semi-transparente
// avec une flèche à l'extrémité gauche et un losange à l'extrémité droite :
Shape arrow = new Shape(doc, ShapeType.Line);
arrow.Width = 200;
arrow.Stroke.Color = Color.Red;
arrow.Stroke.StartArrowType = ArrowType.Arrow;
arrow.Stroke.StartArrowLength = ArrowLength.Long;
arrow.Stroke.StartArrowWidth = ArrowWidth.Wide;
arrow.Stroke.EndArrowType = ArrowType.Diamond;
arrow.Stroke.EndArrowLength = ArrowLength.Long;
arrow.Stroke.EndArrowWidth = ArrowWidth.Wide;
arrow.Stroke.DashStyle = DashStyle.Dash;
arrow.Stroke.Opacity = 0.5;

Assert.AreEqual(JoinStyle.Miter, arrow.Stroke.JoinStyle);

builder.InsertNode(arrow);

// 2 - Ligne diagonale noire épaisse aux extrémités arrondies :
Shape line = new Shape(doc, ShapeType.Line);
line.Top = 40;
line.Width = 200;
line.Height = 20;
line.StrokeWeight = 5.0;
line.Stroke.EndCap = EndCap.Round;

builder.InsertNode(line);

// 3 - Flèche avec un remplissage vert :
Shape filledInArrow = new Shape(doc, ShapeType.Arrow);
filledInArrow.Width = 200;
filledInArrow.Height = 40;
filledInArrow.Top = 100;
filledInArrow.Fill.ForeColor = Color.Green;
filledInArrow.Fill.Visible = true;

builder.InsertNode(filledInArrow);

// 4 - Flèche avec une orientation inversée remplie avec le logo Aspose :
Shape filledInArrowImg = new Shape(doc, ShapeType.Arrow);
filledInArrowImg.Width = 200;
filledInArrowImg.Height = 40;
filledInArrowImg.Top = 160;
filledInArrowImg.FlipOrientation = FlipOrientation.Both;

byte[] imageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(imageBytes))
{
    Image image = Image.FromStream(stream);
    // Lorsque nous inversons l'orientation de notre flèche, nous inversons également l'image que contient la flèche.
    // Retournez l'image dans l'autre sens pour annuler cela avant d'obtenir la forme pour l'afficher.
    image.RotateFlip(RotateFlipType.RotateNoneFlipXY);

    filledInArrowImg.ImageData.SetImage(image);
    filledInArrowImg.Stroke.JoinStyle = JoinStyle.Round;

    builder.InsertNode(filledInArrowImg);
}

doc.Save(ArtifactsDir + "Drawing.VariousShapes.docx");
```

### Voir également

* property [StartArrowType](../stroke/startarrowtype/)
* property [EndArrowType](../stroke/endarrowtype/)
* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
