---
title: Stroke.StartArrowLength
linktitle: StartArrowLength
articleTitle: StartArrowLength
second_title: Aspose.Words para .NET
description: Descubra la propiedad Stroke StartArrowLength para personalizar la longitud de la punta de flecha de su diseño, mejorando el atractivo visual y la precisión en sus proyectos.
type: docs
weight: 210
url: /es/net/aspose.words.drawing/stroke/startarrowlength/
---
## Stroke.StartArrowLength property

Define la longitud de la punta de flecha para el inicio de un trazo.

```csharp
public ArrowLength StartArrowLength { get; set; }
```

## Observaciones

El valor predeterminado esMedium.

## Ejemplos

Muestra cómo crear una variedad de formas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

A continuación se muestran cuatro ejemplos de formas que podemos insertar en nuestros documentos.
// 1 - Línea roja punteada, horizontal y semitransparente
// con una flecha en el extremo izquierdo y un diamante en el extremo derecho:
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

// 2 - Línea diagonal negra gruesa con extremos redondeados:
Shape line = new Shape(doc, ShapeType.Line);
line.Top = 40;
line.Width = 200;
line.Height = 20;
line.StrokeWeight = 5.0;
line.Stroke.EndCap = EndCap.Round;

builder.InsertNode(line);

// 3 - Flecha con relleno verde:
Shape filledInArrow = new Shape(doc, ShapeType.Arrow);
filledInArrow.Width = 200;
filledInArrow.Height = 40;
filledInArrow.Top = 100;
filledInArrow.Fill.ForeColor = Color.Green;
filledInArrow.Fill.Visible = true;

builder.InsertNode(filledInArrow);

// 4 - Flecha con orientación invertida rellena con el logotipo de Aspose:
Shape filledInArrowImg = new Shape(doc, ShapeType.Arrow);
filledInArrowImg.Width = 200;
filledInArrowImg.Height = 40;
filledInArrowImg.Top = 160;
filledInArrowImg.FlipOrientation = FlipOrientation.Both;

byte[] imageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(imageBytes))
{
    Image image = Image.FromStream(stream);
    // Cuando cambiamos la orientación de nuestra flecha, también cambiamos la imagen que contiene la flecha.
    // Gira la imagen hacia el otro lado para cancelar esto antes de que la forma la muestre.
    image.RotateFlip(RotateFlipType.RotateNoneFlipXY);

    filledInArrowImg.ImageData.SetImage(image);
    filledInArrowImg.Stroke.JoinStyle = JoinStyle.Round;

    builder.InsertNode(filledInArrowImg);
}

doc.Save(ArtifactsDir + "Drawing.VariousShapes.docx");
```

### Ver también

* enum [ArrowLength](../../arrowlength/)
* class [Stroke](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
