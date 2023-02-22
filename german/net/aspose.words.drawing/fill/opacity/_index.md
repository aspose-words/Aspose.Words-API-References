---
title: Fill.Opacity
second_title: Aspose.Words für .NET-API-Referenz
description: Fill eigendom. Ruft den Deckkraftgrad der angegebenen Füllung als Wert zwischen 00 durchsichtig und 10 undurchsichtig ab oder legt ihn fest.
type: docs
weight: 90
url: /de/net/aspose.words.drawing/fill/opacity/
---
## Fill.Opacity property

Ruft den Deckkraftgrad der angegebenen Füllung als Wert zwischen 0,0 (durchsichtig) und 1,0 (undurchsichtig) ab oder legt ihn fest.

```csharp
public double Opacity { get; set; }
```

### Bemerkungen

Diese Eigenschaft ist das Gegenteil von Eigenschaft[`Transparency`](../transparency/).

### Beispiele

Zeigt, wie eine Form mit einer Volltonfarbe gefüllt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Schreiben Sie etwas Text und bedecken Sie ihn dann mit einer schwebenden Form.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Verwenden Sie die Eigenschaft "StrokeColor", um die Farbe des Umrisses der Form festzulegen.
shape.StrokeColor = Color.CadetBlue;

// Verwenden Sie die Eigenschaft "FillColor", um die Farbe des Innenbereichs der Form festzulegen.
shape.FillColor = Color.LightBlue;

// Die Eigenschaft "Deckkraft" bestimmt, wie transparent die Farbe auf einer Skala von 0-1 ist,
// wobei 1 vollständig undurchsichtig und 0 unsichtbar ist.
// Die Formfüllung ist standardmäßig vollständig undurchsichtig, sodass wir den Text, auf dem sich diese Form befindet, nicht sehen können.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Setzen Sie die Deckkraft der Füllfarbe der Form auf einen niedrigeren Wert, damit wir den Text darunter sehen können.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Siehe auch

* class [Fill](../)
* namensraum [Aspose.Words.Drawing](../../fill/)
* Montage [Aspose.Words](../../../)


