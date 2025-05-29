---
title: Stroke.BaseForeColor
linktitle: BaseForeColor
articleTitle: BaseForeColor
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Stroke BaseForeColor för att enkelt komma åt den omodifierade basförgrundsfärgen för ditt streck för exakt designkontroll.
type: docs
weight: 40
url: /sv/net/aspose.words.drawing/stroke/baseforecolor/
---
## Stroke.BaseForeColor property

Hämtar den grundläggande förgrundsfärgen för linjen utan några modifierare.

```csharp
public Color BaseForeColor { get; }
```

## Anmärkningar

Standardvärdet för en[`Shape`](../../shape/) är Black .

## Exempel

Visar hur man får förgrundsfärg utan modifierare.

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

### Se även

* class [Stroke](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
