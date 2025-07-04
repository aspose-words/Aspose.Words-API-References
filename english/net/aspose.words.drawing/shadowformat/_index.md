---
title: ShadowFormat Class
linktitle: ShadowFormat
articleTitle: ShadowFormat
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Drawing.ShadowFormat for enhanced object shadow effects. Elevate your document design with customizable shadow formatting options.
type: docs
weight: 1610
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

Assert.That(shadowFormat.Color.ToArgb(), Is.EqualTo(Color.Red.ToArgb()));
Assert.That(shadowFormat.Type, Is.EqualTo(ShadowType.ShadowMixed));
```

### See Also

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
