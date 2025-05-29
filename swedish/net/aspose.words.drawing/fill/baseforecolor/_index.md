---
title: Fill.BaseForeColor
linktitle: BaseForeColor
articleTitle: BaseForeColor
second_title: Aspose.Words för .NET
description: Upptäck egenskapen BaseForeColor för att få åtkomst till ett Color-objekt som representerar den verkliga förgrundsfärgen för din fyllning, vilket förbättrar din designs tydlighet och attraktionskraft.
type: docs
weight: 40
url: /sv/net/aspose.words.drawing/fill/baseforecolor/
---
## Fill.BaseForeColor property

Hämtar ett Color-objekt som representerar basförgrundsfärgen för fill utan några modifierare.

```csharp
public Color BaseForeColor { get; }
```

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

* class [Fill](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
