---
title: ShadowFormat.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: Explore the ShadowFormat Type property to easily customize your shadow effects. Get or set the ShadowType for enhanced design flexibility.
type: docs
weight: 20
url: /net/aspose.words.drawing/shadowformat/type/
---
## ShadowFormat.Type property

Gets or sets the specified [`ShadowType`](../../shadowtype/) for ShadowFormat.

```csharp
public ShadowType Type { get; set; }
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

* enum [ShadowType](../../shadowtype/)
* class [ShadowFormat](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
