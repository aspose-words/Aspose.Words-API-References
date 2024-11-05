---
title: LayoutFlow Enum
linktitle: LayoutFlow
articleTitle: LayoutFlow
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.LayoutFlow enum. Determines the flow of the text layout in a textbox in C#.
type: docs
weight: 1370
url: /net/aspose.words.drawing/layoutflow/
---
## LayoutFlow enumeration

Determines the flow of the text layout in a textbox.

```csharp
public enum LayoutFlow
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Horizontal | `0` | Text is displayed horizontally. |
| TopToBottomIdeographic | `1` | Ideographic text is displayed vertically. |
| BottomToTop | `2` | Text is displayed vertically. |
| TopToBottom | `3` | Text is displayed vertically. |
| HorizontalIdeographic | `4` | Ideographic text is displayed horizontally. |
| Vertical | `5` | Text is displayed vertically. |

## Examples

Shows how to add text to a text box, and change its orientation

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textbox = new Shape(doc, ShapeType.TextBox)
{
    Width = 100,
    Height = 100
};
textbox.TextBox.LayoutFlow = LayoutFlow.BottomToTop;

textbox.AppendChild(new Paragraph(doc));
builder.InsertNode(textbox);

builder.MoveTo(textbox.FirstParagraph);
builder.Write("This text is flipped 90 degrees to the left.");

doc.Save(ArtifactsDir + "Drawing.TextBox.docx");
```

### See Also

* property [LayoutFlow](../textbox/layoutflow/)
* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
