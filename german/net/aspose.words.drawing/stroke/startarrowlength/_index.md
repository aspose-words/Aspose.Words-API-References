---
title: Stroke.StartArrowLength
second_title: Aspose.Words für .NET-API-Referenz
description: Stroke eigendom. Definiert die Pfeilspitzenlänge für den Beginn eines Strichs.
type: docs
weight: 150
url: /de/net/aspose.words.drawing/stroke/startarrowlength/
---
## Stroke.StartArrowLength property

Definiert die Pfeilspitzenlänge für den Beginn eines Strichs.

```csharp
public ArrowLength StartArrowLength { get; set; }
```

### Bemerkungen

Der Standardwert istMedium.

### Beispiele

Zeigt, um eine Vielzahl von Formen zu erstellen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nachfolgend finden Sie vier Beispiele für Formen, die wir in unsere Dokumente einfügen können.
// 1 - Gepunktete, horizontale, halbtransparente rote Linie
// mit einem Pfeil am linken Ende und einer Raute am rechten Ende:
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

// 2 - Dicke schwarze diagonale Linie mit abgerundeten Enden:
Shape line = new Shape(doc, ShapeType.Line);
line.Top = 40;
line.Width = 200;
line.Height = 20;
line.StrokeWeight = 5.0;
line.Stroke.EndCap = EndCap.Round;

builder.InsertNode(line);

// 3 - Pfeil mit grüner Füllung:
Shape filledInArrow = new Shape(doc, ShapeType.Arrow);
filledInArrow.Width = 200;
filledInArrow.Height = 40;
filledInArrow.Top = 100;
filledInArrow.Fill.ForeColor = Color.Green;
filledInArrow.Fill.Visible = true;

builder.InsertNode(filledInArrow);

// 4 - Pfeil mit umgekehrter Ausrichtung, gefüllt mit dem Aspose-Logo:
Shape filledInArrowImg = new Shape(doc, ShapeType.Arrow);
filledInArrowImg.Width = 200;
filledInArrowImg.Height = 40;
filledInArrowImg.Top = 160;
filledInArrowImg.FlipOrientation = FlipOrientation.Both;

byte[] imageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(imageBytes))
{
    Image image = Image.FromStream(stream);
    // Wenn wir die Ausrichtung unseres Pfeils umkehren, kehren wir auch das Bild um, das der Pfeil enthält.
    // Spiegeln Sie das Bild in die andere Richtung, um dies aufzuheben, bevor Sie die Form erhalten, um es anzuzeigen.
    image.RotateFlip(RotateFlipType.RotateNoneFlipXY);

    filledInArrowImg.ImageData.SetImage(image);
    filledInArrowImg.Stroke.JoinStyle = JoinStyle.Round;

    builder.InsertNode(filledInArrowImg);
}

doc.Save(ArtifactsDir + "Drawing.VariousShapes.docx");
```

### Siehe auch

* enum [ArrowLength](../../arrowlength/)
* class [Stroke](../)
* namensraum [Aspose.Words.Drawing](../../stroke/)
* Montage [Aspose.Words](../../../)


