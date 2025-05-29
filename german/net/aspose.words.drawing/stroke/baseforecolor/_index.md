---
title: Stroke.BaseForeColor
linktitle: BaseForeColor
articleTitle: BaseForeColor
second_title: Aspose.Words für .NET
description: Entdecken Sie die Stroke BaseForeColor-Eigenschaft, um einfach auf die unveränderte Basisvordergrundfarbe Ihres Strichs zuzugreifen und so eine präzise Designkontrolle zu erreichen.
type: docs
weight: 40
url: /de/net/aspose.words.drawing/stroke/baseforecolor/
---
## Stroke.BaseForeColor property

Ruft die grundlegende Vordergrundfarbe des Strichs ohne Modifikatoren ab.

```csharp
public Color BaseForeColor { get; }
```

## Bemerkungen

Der Standardwert für eine[`Shape`](../../shape/) ist Black .

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

* class [Stroke](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
