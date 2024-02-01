---
title: TextBoxWrapMode Enum
linktitle: TextBoxWrapMode
articleTitle: TextBoxWrapMode
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.TextBoxWrapMode enum. Specifies how text wraps inside a shape in C#.
type: docs
weight: 1440
url: /net/aspose.words.drawing/textboxwrapmode/
---
## TextBoxWrapMode enumeration

Specifies how text wraps inside a shape.

```csharp
public enum TextBoxWrapMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Square | `0` | Text wraps inside a shape. |
| None | `2` | Text does not wrap inside a shape. |

## Examples

Shows how to set a wrapping mode for the contents of a text box.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 300, 300);
TextBox textBox = textBoxShape.TextBox;

// Set the "TextBoxWrapMode" property to "TextBoxWrapMode.None" to increase the text box's width
// to accommodate text, should it be large enough.
// Set the "TextBoxWrapMode" property to "TextBoxWrapMode.Square" to
// wrap all text inside the text box, preserving its dimensions.
textBox.TextBoxWrapMode = textBoxWrapMode;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Font.Size = 32;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "Shape.TextBoxContentsWrapMode.docx");
```

### See Also

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
