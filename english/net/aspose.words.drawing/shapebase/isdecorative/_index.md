---
title: ShapeBase.IsDecorative
linktitle: IsDecorative
articleTitle: IsDecorative
second_title: Aspose.Words for .NET
description: Discover ShapeBase. Easily manage decorative properties in your documents. Enhance visual appeal by setting flags for unique shape designs.
type: docs
weight: 260
url: /net/aspose.words.drawing/shapebase/isdecorative/
---
## ShapeBase.IsDecorative property

Gets or sets the flag that specifies whether the shape is decorative in the document.

```csharp
public bool IsDecorative { get; set; }
```

## Remarks

Note that shape having not empty [`AlternativeText`](../alternativetext/) cannot be decorative.

## Examples

Shows how to set that the shape is decorative.

```csharp
Document doc = new Document(MyDir + "Decorative shapes.docx");

Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.That(shape.IsDecorative, Is.True);

// If "AlternativeText" is not empty, the shape cannot be decorative.
// That's why our value has changed to 'false'.
shape.AlternativeText = "Alternative text.";
Assert.That(shape.IsDecorative, Is.False);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
// Create a new shape as decorative.
shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.IsDecorative = true;

doc.Save(ArtifactsDir + "Shape.IsDecorative.docx");
```

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
