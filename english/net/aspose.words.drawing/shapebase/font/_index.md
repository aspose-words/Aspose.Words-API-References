---
title: ShapeBase.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words for .NET
description: Discover the ShapeBase Font property for easy font formatting access. Enhance your designs with customizable text styles and unique typography options.
type: docs
weight: 190
url: /net/aspose.words.drawing/shapebase/font/
---
## ShapeBase.Font property

Provides access to the font formatting of this object.

```csharp
public Font Font { get; }
```

## Examples

Shows how to insert a text box, and set the font of its contents.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.TextBox, 300, 50);
builder.MoveTo(shape.LastParagraph);
builder.Write("This text is inside the text box.");

// Set the "Hidden" property of the shape's "Font" object to "true" to hide the text box from sight
// and collapse the space that it would normally occupy.
// Set the "Hidden" property of the shape's "Font" object to "false" to leave the text box visible.
shape.Font.Hidden = hideShape;

// If the shape is visible, we will modify its appearance via the font object.
if (!hideShape)
{
    shape.Font.HighlightColor = Color.LightGray;
    shape.Font.Color = Color.Red;
    shape.Font.Underline = Underline.Dash;
}

// Move the builder out of the text box back into the main document.
builder.MoveTo(shape.ParentParagraph);

builder.Writeln("\nThis text is outside the text box.");

doc.Save(ArtifactsDir + "Shape.Font.docx");
```

### See Also

* class [Font](../../../aspose.words/font/)
* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
