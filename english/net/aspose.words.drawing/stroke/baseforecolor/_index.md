---
title: Stroke.BaseForeColor
linktitle: BaseForeColor
articleTitle: BaseForeColor
second_title: Aspose.Words for .NET
description: Discover the Stroke BaseForeColor property to easily access the unmodified base foreground color of your stroke for precise design control.
type: docs
weight: 40
url: /net/aspose.words.drawing/stroke/baseforecolor/
---
## Stroke.BaseForeColor property

Gets the base foreground color of the stroke without any modifiers.

```csharp
public Color BaseForeColor { get; }
```

## Remarks

The default value for a [`Shape`](../../shape/) is Black.

## Examples

Shows how to get foreground color without modifiers.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 40);
shape.Fill.ForeColor = Color.Red;
shape.Fill.ForeTintAndShade = 0.5;
shape.Stroke.Fill.ForeColor = Color.Green;
shape.Stroke.Fill.Transparency = 0.5;

Assert.That(shape.Fill.ForeColor.ToArgb(), Is.EqualTo(Color.FromArgb(255, 255, 188, 188).ToArgb()));
Assert.That(shape.Fill.BaseForeColor.ToArgb(), Is.EqualTo(Color.Red.ToArgb()));

Assert.That(shape.Stroke.ForeColor.ToArgb(), Is.EqualTo(Color.FromArgb(128, 0, 128, 0).ToArgb()));
Assert.That(shape.Stroke.BaseForeColor.ToArgb(), Is.EqualTo(Color.Green.ToArgb()));

Assert.That(shape.Stroke.Fill.ForeColor.ToArgb(), Is.EqualTo(Color.Green.ToArgb()));
Assert.That(shape.Stroke.Fill.BaseForeColor.ToArgb(), Is.EqualTo(Color.Green.ToArgb()));
```

### See Also

* class [Stroke](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
