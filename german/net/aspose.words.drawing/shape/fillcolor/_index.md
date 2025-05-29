---
title: Shape.FillColor
linktitle: FillColor
articleTitle: FillColor
second_title: Aspose.Words für .NET
description: Entdecken Sie die Shape FillColor-Eigenschaft, um Ihre Designs mit lebendigen Pinselfarben anzupassen, die Ihre Formen hervorheben und Ihre Projekte aufwerten.
type: docs
weight: 50
url: /de/net/aspose.words.drawing/shape/fillcolor/
---
## Shape.FillColor property

Definiert die Pinselfarbe, die den geschlossenen Pfad der Form füllt.

```csharp
public Color FillColor { get; set; }
```

## Bemerkungen

Dies ist eine Abkürzung zum[`Color`](../../fill/color/) Eigentum.

Der Standardwert ist White .

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

* class [Shape](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
