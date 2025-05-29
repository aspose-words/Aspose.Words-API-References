---
title: Fill.BaseForeColor
linktitle: BaseForeColor
articleTitle: BaseForeColor
second_title: Aspose.Words für .NET
description: Entdecken Sie die BaseForeColor-Eigenschaft, um auf ein Color-Objekt zuzugreifen, das die wahre Vordergrundfarbe für Ihre Füllung darstellt und so die Klarheit und Attraktivität Ihres Designs verbessert.
type: docs
weight: 40
url: /de/net/aspose.words.drawing/fill/baseforecolor/
---
## Fill.BaseForeColor property

Ruft ein Farbobjekt ab, das die Basisvordergrundfarbe für die Füllung ohne Modifikatoren darstellt.

```csharp
public Color BaseForeColor { get; }
```

## Beispiele

Zeigt, wie man Vordergrundfarbe ohne Modifikatoren erhält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 40);
shape.Fill.ForeColor = Color.Red;
shape.Fill.ForeTintAndShade = 0.5;
shape.Stroke.Fill.ForeColor = Color.Green;
shape.Stroke.Fill.Transparency = 0.5;

Assert.AreEqual(Color.FromArgb(255, 255, 188, 188).ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.BaseForeColor.ToArgb());

Assert.AreEqual(Color.FromArgb(128, 0, 128, 0).ToArgb(), shape.Stroke.ForeColor.ToArgb());
Assert.AreEqual(Color.Green.ToArgb(), shape.Stroke.BaseForeColor.ToArgb());

Assert.AreEqual(Color.Green.ToArgb(), shape.Stroke.Fill.ForeColor.ToArgb());
Assert.AreEqual(Color.Green.ToArgb(), shape.Stroke.Fill.BaseForeColor.ToArgb());
```

### Siehe auch

* class [Fill](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
