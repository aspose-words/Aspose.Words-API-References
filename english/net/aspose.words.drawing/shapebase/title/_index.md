---
title: ShapeBase.Title
linktitle: Title
second_title: Aspose.Words for .NET API Reference
description: ShapeBase property. Gets or sets the title caption of the current shape object in C#.
type: docs
weight: 530
url: /net/aspose.words.drawing/shapebase/title/
---
## ShapeBase.Title property

Gets or sets the title (caption) of the current shape object.

```csharp
public string Title { get; set; }
```

## Remarks

Default is empty string.

Cannot be `null`, but can be an empty string.

## Examples

Shows how to set the title of a shape.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create a shape, give it a title, and then add it to the document.
Shape shape = new Shape(doc, ShapeType.Cube);
shape.Width = 200;
shape.Height = 200;
shape.Title = "My cube";

builder.InsertNode(shape);

// When we save a document with a shape that has a title,
// Aspose.Words will store that title in the shape's Alt Text.
doc.Save(ArtifactsDir + "Shape.Title.docx");

doc = new Document(ArtifactsDir + "Shape.Title.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(string.Empty, shape.Title);
Assert.AreEqual("Title: My cube", shape.AlternativeText);
```

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../shapebase/)
* assembly [Aspose.Words](../../../)
