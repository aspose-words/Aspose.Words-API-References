---
title: ShapeBase.ShadowFormat
linktitle: ShadowFormat
articleTitle: ShadowFormat
second_title: Aspose.Words for .NET
description: Discover the ShapeBase ShadowFormat property to enhance your designs with customizable shadow effects for shapes. Elevate your visual appeal today!
type: docs
weight: 520
url: /net/aspose.words.drawing/shapebase/shadowformat/
---
## ShapeBase.ShadowFormat property

Gets shadow formatting for the shape.

```csharp
public ShadowFormat ShadowFormat { get; }
```

## Examples

Shows how to get shadow color.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShadowFormat shadowFormat = shape.ShadowFormat;

Assert.AreEqual(Color.Red.ToArgb(), shadowFormat.Color.ToArgb());
Assert.AreEqual(ShadowType.ShadowMixed, shadowFormat.Type);
```

### See Also

* class [ShadowFormat](../../shadowformat/)
* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
