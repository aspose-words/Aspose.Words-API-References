---
title: ShadowFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words for .NET
description: Discover the ShadowFormat Color property to customize shadow colors in your designs. Default is Black, but unleash your creativity with vibrant options!
type: docs
weight: 10
url: /net/aspose.words.drawing/shadowformat/color/
---
## ShadowFormat.Color property

Gets a Color object that represents the color for the shadow. The default value is Black.

```csharp
public Color Color { get; }
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

* class [ShadowFormat](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
