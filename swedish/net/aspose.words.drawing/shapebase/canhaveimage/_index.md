---
title: ShapeBase.CanHaveImage
linktitle: CanHaveImage
articleTitle: CanHaveImage
second_title: Aspose.Words för .NET
description: ShapeBase CanHaveImage fast egendom. ReturnerarSann om formtypen tillåter att formen har en bild i C#.
type: docs
weight: 100
url: /sv/net/aspose.words.drawing/shapebase/canhaveimage/
---
## ShapeBase.CanHaveImage property

Returnerar`Sann` om formtypen tillåter att formen har en bild.

```csharp
public bool CanHaveImage { get; }
```

## Anmärkningar

Även om Microsoft Word har en speciell formtyp för bilder, verkar det som att i Microsoft Word-dokument kan alla shape förutom en gruppform ha en bild, därför returnerar den här egenskapen`Sann` för alla former utom[`GroupShape`](../../groupshape/).

## Exempel

Visar hur man infogar och roterar en bild.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en form med en bild.
Shape shape = builder.InsertImage(Image.FromFile(ImageDir + "Logo.jpg"));
Assert.True(shape.CanHaveImage);
Assert.True(shape.HasImage);

// Rotera bilden 45 grader medurs.
shape.Rotation = 45;

doc.Save(ArtifactsDir + "Shape.Rotate.docx");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
