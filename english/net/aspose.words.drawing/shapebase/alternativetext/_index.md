---
title: ShapeBase.AlternativeText
linktitle: AlternativeText
articleTitle: AlternativeText
second_title: Aspose.Words for .NET
description: ShapeBase AlternativeText property. Defines alternative text to be displayed instead of a graphic in C#.
type: docs
weight: 20
url: /net/aspose.words.drawing/shapebase/alternativetext/
---
## ShapeBase.AlternativeText property

Defines alternative text to be displayed instead of a graphic.

```csharp
public string AlternativeText { get; set; }
```

## Remarks

The default value is an empty string.

## Examples

Shows how to use a shape's alternative text.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertShape(ShapeType.Cube, 150, 150);
shape.Name = "MyCube";

shape.AlternativeText = "Alt text for MyCube.";

// We can access the alternative text of a shape by right-clicking it, and then via "Format AutoShape" -> "Alt Text".
doc.Save(ArtifactsDir + "Shape.AltText.docx");

// Save the document to HTML, and then delete the linked image that belongs to our shape.
// The browser that is reading our HTML will display the alt text in place of the missing image.
doc.Save(ArtifactsDir + "Shape.AltText.html");
File.Delete(ArtifactsDir + "Shape.AltText.001.png");
```

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
