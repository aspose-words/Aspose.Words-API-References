---
title: ShapeBase.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words för .NET
description: Upptäck ShapeBase Rotation-egenskapen, definiera och anpassa enkelt rotationsvinklar för dina former, vilket förbättrar din designs precision och kreativitet.
type: docs
weight: 500
url: /sv/net/aspose.words.drawing/shapebase/rotation/
---
## ShapeBase.Rotation property

Definierar vinkeln (i grader) som en form roteras med. Positivt värde motsvarar medurs rotationsvinkel.

```csharp
public double Rotation { get; set; }
```

## Anmärkningar

Standardvärdet är 0.

## Exempel

Visar hur man infogar och roterar en bild.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en form med en bild.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
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
