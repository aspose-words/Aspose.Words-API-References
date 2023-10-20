---
title: ShapeBase.FlipOrientation
linktitle: FlipOrientation
articleTitle: FlipOrientation
second_title: Aspose.Words för .NET
description: ShapeBase FlipOrientation fast egendom. Ändrar orienteringen för en form i C#.
type: docs
weight: 180
url: /sv/net/aspose.words.drawing/shapebase/fliporientation/
---
## ShapeBase.FlipOrientation property

Ändrar orienteringen för en form.

```csharp
public FlipOrientation FlipOrientation { get; set; }
```

## Anmärkningar

Standardvärdet ärNone.

## Exempel

Visar hur man vänder en form på en axel.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en bildform och lämna dess orientering i standardläge.
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

Assert.AreEqual(FlipOrientation.None, shape.FlipOrientation);

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Ställ in egenskapen "FlipOrientation" till "FlipOrientation.Horizontal" för att vända den andra formen på y-axeln,
// gör det till en horisontell spegelbild av den första formen.
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
// gör det till en horisontell och vertikal spegelbild av den första formen.
shape.FlipOrientation = FlipOrientation.Both;

doc.Save(ArtifactsDir + "Shape.FlipShapeOrientation.docx");
```

### Se även

* enum [FlipOrientation](../../fliporientation/)
* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
