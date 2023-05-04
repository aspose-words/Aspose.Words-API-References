---
title: TextBox.VerticalAnchor
linktitle: VerticalAnchor
articleTitle: VerticalAnchor
second_title: Aspose.Words for .NET
description: TextBox VerticalAnchor property. Specifies the vertical alignment of the text within a shape in C#.
type: docs
weight: 120
url: /net/aspose.words.drawing/textbox/verticalanchor/
---
## TextBox.VerticalAnchor property

Specifies the vertical alignment of the text within a shape.

```csharp
public TextBoxAnchor VerticalAnchor { get; set; }
```

## Remarks

The default value is Top.

## Examples

Shows how to vertically align the text contents of a text box.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// Set the "VerticalAnchor" property to "TextBoxAnchor.Top" to
// align the text in this text box with the top side of the shape.
// Set the "VerticalAnchor" property to "TextBoxAnchor.Middle" to
// align the text in this text box to the center of the shape.
// Set the "VerticalAnchor" property to "TextBoxAnchor.Bottom" to
// align the text in this text box to the bottom of the shape.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// The vertical aligning of text inside text boxes is available from Microsoft Word 2007 onwards.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### See Also

* enum [TextBoxAnchor](../../textboxanchor/)
* class [TextBox](../)
* namespace [Aspose.Words.Drawing](../../textbox/)
* assembly [Aspose.Words](../../../)
