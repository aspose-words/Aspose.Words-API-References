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

Gets or sets a Color object that represents the color for the shadow. The default value is Black.

```csharp
public Color Color { get; set; }
```

## Examples

Shows how to get shadow color.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShadowFormat shadowFormat = shape.ShadowFormat;

Assert.That(shadowFormat.Color.ToArgb(), Is.EqualTo(Color.Red.ToArgb()));
Assert.That(shadowFormat.Type, Is.EqualTo(ShadowType.ShadowMixed));
```

Shows how to set a color with transparency.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

ShadowFormat shadowFormat = shape.ShadowFormat;
shadowFormat.Type = ShadowType.Shadow21;
shadowFormat.Color = Color.Red;
shadowFormat.Transparency = 0.8;

doc.Save(ArtifactsDir + "Shape.ShadowFormatTransparency.docx");
```

### See Also

* class [ShadowFormat](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
