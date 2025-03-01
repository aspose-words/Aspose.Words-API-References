---
title: ShapeBase.IsTopLevel
linktitle: IsTopLevel
articleTitle: IsTopLevel
second_title: Aspose.Words for .NET
description: Discover ShapeBase IsTopLevel. Quickly verify if a shape stands alone, enhancing your design workflow with efficient group management.
type: docs
weight: 370
url: /net/aspose.words.drawing/shapebase/istoplevel/
---
## ShapeBase.IsTopLevel property

Returns `true` if this shape is not a child of a group shape.

```csharp
public bool IsTopLevel { get; }
```

## Examples

Shows how to tell whether a shape is a part of a group shape.

```csharp
Document doc = new Document();

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
shape.WrapType = WrapType.None;

// A shape by default is not part of any group shape, and therefore has the "IsTopLevel" property set to "true".
Assert.True(shape.IsTopLevel);

GroupShape group = new GroupShape(doc);
group.AppendChild(shape);

// Once we assimilate a shape into a group shape, the "IsTopLevel" property changes to "false".
Assert.False(shape.IsTopLevel);
```

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
