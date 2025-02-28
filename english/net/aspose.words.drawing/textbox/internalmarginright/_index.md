---
title: TextBox.InternalMarginRight
linktitle: InternalMarginRight
articleTitle: InternalMarginRight
second_title: Aspose.Words for .NET
description: Discover the TextBox InternalMarginRight property to customize your shapes with precise right margins in points for enhanced design flexibility.
type: docs
weight: 40
url: /net/aspose.words.drawing/textbox/internalmarginright/
---
## TextBox.InternalMarginRight property

Specifies the inner right margin in points for a shape.

```csharp
public double InternalMarginRight { get; set; }
```

## Remarks

The default value is 1/10 inch.

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
