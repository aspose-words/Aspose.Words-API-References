---
title: ShapeBase.Hidden
linktitle: Hidden
articleTitle: Hidden
second_title: Aspose.Words for .NET
description: Control shape visibility with ShapeBase's hidden property. Easily toggle between visible and hidden for enhanced design flexibility.
type: docs
weight: 230
url: /net/aspose.words.drawing/shapebase/hidden/
---
## ShapeBase.Hidden property

Gets or sets a boolean value indicating whether the shape is visible.

```csharp
public bool Hidden { get; set; }
```

## Remarks

The default value is `false`.

## Examples

Shows how to hide the shape.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
if (!shape.Hidden)
    shape.Hidden = true;

doc.Save(ArtifactsDir + "Shape.Hidden.docx");
```

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
