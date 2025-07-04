---
title: Fill.BaseForeColor
linktitle: BaseForeColor
articleTitle: BaseForeColor
second_title: Aspose.Words for .NET
description: Discover the BaseForeColor property to access a Color object representing the true foreground color for your fill, enhancing your design's clarity and appeal.
type: docs
weight: 40
url: /net/aspose.words.drawing/fill/baseforecolor/
---
## Fill.BaseForeColor property

Gets a Color object that represents the base foreground color for the fill without any modifiers.

```csharp
public Color BaseForeColor { get; }
```

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

* class [Fill](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
