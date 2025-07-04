---
title: ShapeBase.SoftEdge
linktitle: SoftEdge
articleTitle: SoftEdge
second_title: Aspose.Words for .NET
description: Enhance your designs with ShapeBase SoftEdge for smooth, soft edge formatting. Elevate your visuals effortlessly and stand out in every project!
type: docs
weight: 550
url: /net/aspose.words.drawing/shapebase/softedge/
---
## ShapeBase.SoftEdge property

Gets soft edge formatting for the shape.

```csharp
public SoftEdgeFormat SoftEdge { get; }
```

## Examples

Shows how to set limit for image resolution.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.MaxImageResolution = 72;

doc.Save(ArtifactsDir + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

Shows how to work with soft edge formatting.

```csharp
DocumentBuilder builder = new DocumentBuilder();
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 200);

// Apply soft edge to the shape.
shape.SoftEdge.Radius = 30;

builder.Document.Save(ArtifactsDir + "Shape.SoftEdge.docx");

// Load document with rectangle shape with soft edge.
Document doc = new Document(ArtifactsDir + "Shape.SoftEdge.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
SoftEdgeFormat softEdgeFormat = shape.SoftEdge;

// Check soft edge radius.
Assert.That(softEdgeFormat.Radius, Is.EqualTo(30));

// Remove soft edge from the shape.
softEdgeFormat.Remove();

// Check radius of the removed soft edge.
Assert.That(softEdgeFormat.Radius, Is.EqualTo(0));
```

### See Also

* class [SoftEdgeFormat](../../softedgeformat/)
* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
