---
title: ArrowType Enum
linktitle: ArrowType
articleTitle: ArrowType
second_title: Aspose.Words pour .NET
description: Aspose.Words.Drawing.ArrowType énumération. Spécifie le type dune flèche à la fin dune ligne en C#.
type: docs
weight: 490
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
| Stealth | `2` | La flèche est une flèche "furtive". |
| Diamond | `3` | La fin de la ligne est un diamant solide. |
| Oval | `4` | La fin de la ligne est un ovale plein. |
| Open | `5` | La flèche est une flèche ouverte. |
| Default | `0` | Identique àNone . |

## Exemples

Montre pour créer une variété de formes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous quatre exemples de formes que nous pouvons insérer dans nos documents.
// 1 - Ligne rouge pointillée, horizontale, semi-transparente
// avec une flèche à gauche et un losange à droite :
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

// 2 - Ligne diagonale noire épaisse aux extrémités arrondies :
Shape line = new Shape(doc, ShapeType.Line);
line.Top = 40;
line.Width = 200;
line.Height = 20;
line.StrokeWeight = 5.0;
line.Stroke.EndCap = EndCap.Round;

builder.InsertNode(line);

// 3 - Flèche avec un remplissage vert :
Shape filledInArrow = new Shape(doc, ShapeType.Arrow);
filledInArrow.Width = 200;
filledInArrow.Height = 40;
filledInArrow.Top = 100;
filledInArrow.Fill.ForeColor = Color.Green;
filledInArrow.Fill.Visible = true;

builder.InsertNode(filledInArrow);

// 4 - Flèche d'orientation inversée remplie du logo Aspose :
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
    // Retournez l'image dans l'autre sens pour l'annuler avant que la forme ne l'affiche.
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
