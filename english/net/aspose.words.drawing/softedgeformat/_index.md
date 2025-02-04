---
title: SoftEdgeFormat Class
linktitle: SoftEdgeFormat
articleTitle: SoftEdgeFormat
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.SoftEdgeFormat class. Represents the soft edge formatting for an object in C#.
type: docs
weight: 1700
url: /net/aspose.words.drawing/softedgeformat/
---
## SoftEdgeFormat class

Represents the soft edge formatting for an object.

```csharp
public class SoftEdgeFormat
```

## Properties

| Name | Description |
| --- | --- |
| [Radius](../../aspose.words.drawing/softedgeformat/radius/) { get; set; } | Gets or sets a double value that represents the length of the radius for a soft edge effect in points (pt). The default value is 0.0. |

## Methods

| Name | Description |
| --- | --- |
| [Remove](../../aspose.words.drawing/softedgeformat/remove/)() | Removes `SoftEdgeFormat` from the parent object. |

## Remarks

Use the [`SoftEdge`](../shapebase/softedge/) property to access soft edge properties of an object. You do not create instances of the `SoftEdgeFormat` class directly.

## Examples

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
Assert.AreEqual(30, softEdgeFormat.Radius);

// Remove soft edge from the shape.
softEdgeFormat.Remove();

// Check radius of the removed soft edge.
Assert.AreEqual(0, softEdgeFormat.Radius);
```

### See Also

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
