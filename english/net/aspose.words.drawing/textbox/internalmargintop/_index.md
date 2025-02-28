---
title: TextBox.InternalMarginTop
linktitle: InternalMarginTop
articleTitle: InternalMarginTop
second_title: Aspose.Words for .NET
description: Discover the TextBox InternalMarginTop property—control your shape's top margin in points for precise layout and enhanced design flexibility.
type: docs
weight: 50
url: /net/aspose.words.drawing/textbox/internalmargintop/
---
## TextBox.InternalMarginTop property

Specifies the inner top margin in points for a shape.

```csharp
public double InternalMarginTop { get; set; }
```

## Remarks

The default value is 1/20 inch.

## Examples

Shows how to set internal margins for a text box.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert another textbox with specific margins.
Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox = textBoxShape.TextBox;
textBox.InternalMarginTop = 15;
textBox.InternalMarginBottom = 15;
textBox.InternalMarginLeft = 15;
textBox.InternalMarginRight = 15;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text placed according to textbox margins.");

doc.Save(ArtifactsDir + "Shape.TextBoxMargins.docx");
```

### See Also

* class [TextBox](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
