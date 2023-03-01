---
title: TextBox.TextBoxWrapMode
linktitle: TextBoxWrapMode
second_title: Aspose.Words for .NET API Reference
description: TextBox property. Determines how text wraps inside a shape in C#.
type: docs
weight: 110
url: /net/aspose.words.drawing/textbox/textboxwrapmode/
---
## TextBox.TextBoxWrapMode property

Determines how text wraps inside a shape.

```csharp
public TextBoxWrapMode TextBoxWrapMode { get; set; }
```

## Remarks

The default value is Square.

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

* enum [TextBoxWrapMode](../../textboxwrapmode/)
* class [TextBox](../)
* namespace [Aspose.Words.Drawing](../../textbox/)
* assembly [Aspose.Words](../../../)
