---
title: ShadowFormat Class
linktitle: ShadowFormat
articleTitle: ShadowFormat
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.ShadowFormat class. Represents shadow formatting for an object in C#.
type: docs
weight: 1480
url: /net/aspose.words.drawing/shadowformat/
---
## ShadowFormat class

Represents shadow formatting for an object.

To learn more, visit the [Working with Graphic Elements](https://docs.aspose.com/words/net/working-with-graphic-elements/) documentation article.

```csharp
public class ShadowFormat
```

## Properties

| Name | Description |
| --- | --- |
| [Color](../../aspose.words.drawing/shadowformat/color/) { get; } | Gets a Color object that represents the color for the shadow. The default value is Black. |
| [Type](../../aspose.words.drawing/shadowformat/type/) { get; set; } | Gets or sets the specified [`ShadowType`](../shadowtype/) for ShadowFormat. |
| [Visible](../../aspose.words.drawing/shadowformat/visible/) { get; } | Returns `true` if the formatting applied to this instance is visible. |

## Methods

| Name | Description |
| --- | --- |
| [Clear](../../aspose.words.drawing/shadowformat/clear/)() | Clears shadow format. |

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

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
