---
title: Fill.Opacity
linktitle: Opacity
articleTitle: Opacity
second_title: Aspose.Words für .NET
description: Steuern Sie die Transparenz Ihres Designs mit der Eigenschaft „Füllopazität“ und passen Sie die Klarheit von völlig klar bis völlig undurchsichtig an, um eine beeindruckende Optik zu erzielen.
type: docs
weight: 150
url: /de/net/aspose.words.drawing/fill/opacity/
---
## Fill.Opacity property

Ruft den Grad der Deckkraft der angegebenen Füllung als Wert zwischen 0,0 (klar) und 1,0 (undurchsichtig) ab oder legt ihn fest.

```csharp
public double Opacity { get; set; }
```

## Bemerkungen

Diese Eigenschaft ist das Gegenteil von Eigentum[`Transparency`](../transparency/).

## Beispiele

Zeigt, wie eine Form mit einer Volltonfarbe gefüllt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Schreiben Sie einen Text und bedecken Sie ihn dann mit einer schwebenden Form.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Verwenden Sie die Eigenschaft „StrokeColor“, um die Farbe des Umrisses der Form festzulegen.
shape.StrokeColor = Color.CadetBlue;

// Verwenden Sie die Eigenschaft „FillColor“, um die Farbe des Innenbereichs der Form festzulegen.
shape.FillColor = Color.LightBlue;

// Die Eigenschaft „Deckkraft“ bestimmt, wie transparent die Farbe auf einer Skala von 0 bis 1 ist.
// wobei 1 völlig undurchsichtig und 0 unsichtbar ist.
// Die Formfüllung ist standardmäßig vollständig undurchsichtig, sodass wir den Text, über dem sich diese Form befindet, nicht sehen können.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Stellen Sie die Deckkraft der Formfüllfarbe auf einen niedrigeren Wert ein, damit wir den Text darunter sehen können.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Siehe auch

* class [Fill](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
