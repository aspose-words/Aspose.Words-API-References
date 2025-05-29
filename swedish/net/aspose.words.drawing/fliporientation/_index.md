---
title: FlipOrientation Enum
linktitle: FlipOrientation
articleTitle: FlipOrientation
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Drawing.FlipOrientation-enum för mångsidiga alternativ för formorientering. Förbättra din dokumentdesign med flexibel anpassning!
type: docs
weight: 1290
url: /sv/net/aspose.words.drawing/fliporientation/
---
## FlipOrientation enumeration

Möjliga värden för en forms orientering.

```csharp
[Flags]
public enum FlipOrientation
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Koordinaterna är inte omvända. |
| Horizontal | `1` | Vänd längs y-axeln och kasta om x-koordinaterna. |
| Vertical | `2` | Vänd längs x-axeln och invertera y-koordinaterna. |
| Both | `3` | Vänd längs både y- och x-axeln. |

## Exempel

Visar hur man vänder en form på en axel.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en bildform och lämna dess orientering i standardläget.
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

Assert.AreEqual(FlipOrientation.None, shape.FlipOrientation);

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Ställ in egenskapen "FlipOrientation" till "FlipOrientation.Horizontal" för att vända den andra formen på y-axeln,
// gör den till en horisontell spegelbild av den första formen.
shape.FlipOrientation = FlipOrientation.Horizontal;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Ställ in egenskapen "FlipOrientation" till "FlipOrientation.Horizontal" för att vända den tredje formen på x-axeln,
// gör den till en vertikal spegelbild av den första formen.
shape.FlipOrientation = FlipOrientation.Vertical;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Ställ in egenskapen "FlipOrientation" till "FlipOrientation.Horizontal" för att vända den fjärde formen på både x- och y-axeln,
// gör den till en horisontell och vertikal spegelbild av den första formen.
shape.FlipOrientation = FlipOrientation.Both;

doc.Save(ArtifactsDir + "Shape.FlipShapeOrientation.docx");
```

### Se även

* property [FlipOrientation](../shapebase/fliporientation/)
* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
