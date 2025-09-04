---
title: ShadowFormat.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: Explore the ShadowFormat Type property to easily customize your shadow effects. Get or set the ShadowType for enhanced design flexibility.
type: docs
weight: 30
url: /net/aspose.words.drawing/shadowformat/type/
---
## ShadowFormat.Type property

Gets or sets the specified [`ShadowType`](../../shadowtype/) for ShadowFormat.

```csharp
public ShadowType Type { get; set; }
```

## Remarks

Setting a new shadow type will reset Color and Transparency values to their default ones. Therefore, it makes sense to first set the desired shadow type and only then Color and Transparency values.

## Examples

Shows how to get shadow color.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShadowFormat shadowFormat = shape.ShadowFormat;

Assert.That(shadowFormat.Color.ToArgb(), Is.EqualTo(Color.Red.ToArgb()));
Assert.That(shadowFormat.Type, Is.EqualTo(ShadowType.ShadowMixed));
```

### See Also

* enum [ShadowType](../../shadowtype/)
* class [ShadowFormat](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
