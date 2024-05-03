---
title: SoftEdgeFormat.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words for .NET
description: SoftEdgeFormat Remove method. Removes SoftEdgeFormat from the parent object in C#.
type: docs
weight: 20
url: /net/aspose.words.drawing/softedgeformat/remove/
---
## SoftEdgeFormat.Remove method

Removes [`SoftEdgeFormat`](../) from the parent object.

```csharp
public void Remove()
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

// Check soft edge radius.
Assert.AreEqual(30, shape.SoftEdge.Radius);

// Remove soft edge from the shape.
shape.SoftEdge.Remove();

// Check radius of the removed soft edge.
Assert.AreEqual(0, shape.SoftEdge.Radius);
```

### See Also

* class [SoftEdgeFormat](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
