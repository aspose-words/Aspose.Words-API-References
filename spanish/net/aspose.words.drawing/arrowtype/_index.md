---
title: Enum ArrowType
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Drawing.ArrowType enumeración. Especifica el tipo de flecha al final de una línea.
type: docs
weight: 490
url: /es/net/aspose.words.drawing/arrowtype/
---
## ArrowType enumeration

Especifica el tipo de flecha al final de una línea.

```csharp
public enum ArrowType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | La línea no tiene una flecha al final. |
| Arrow | `1` | La flecha es un triángulo sólido. |
| Stealth | `2` | La flecha es una flecha "sigilosa". |
| Diamond | `3` | El final de la línea es un diamante macizo. |
| Oval | `4` | El final de la línea es un óvalo sólido. |
| Open | `5` | La flecha es una flecha abierta. |
| Default | `0` | Igual queNone . |

### Ejemplos

Muestra para crear una variedad de formas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A continuación se muestran cuatro ejemplos de formas que podemos insertar en nuestros documentos.
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
    // Cuando invertimos la orientación de nuestra flecha, también invertimos la imagen que contiene la flecha.
    // Voltear la imagen hacia el otro lado para cancelar esto antes de obtener la forma para mostrarla.
    image.RotateFlip(RotateFlipType.RotateNoneFlipXY);

    filledInArrowImg.ImageData.SetImage(image);
    filledInArrowImg.Stroke.JoinStyle = JoinStyle.Round;

    builder.InsertNode(filledInArrowImg);
}

doc.Save(ArtifactsDir + "Drawing.VariousShapes.docx");
```

### Ver también

* property [StartArrowType](../stroke/startarrowtype/)
* property [EndArrowType](../stroke/endarrowtype/)
* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)


