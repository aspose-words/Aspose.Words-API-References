---
title: ShapeBase.ParentParagraph
linktitle: ParentParagraph
articleTitle: ParentParagraph
second_title: Aspose.Words for .NET
description: Discover the ShapeBase ParentParagraph property—efficiently access the immediate parent paragraph for streamlined content management and enhanced organization.
type: docs
weight: 430
url: /net/aspose.words.drawing/shapebase/parentparagraph/
---
## ShapeBase.ParentParagraph property

Returns the immediate parent paragraph.

```csharp
public Paragraph ParentParagraph { get; }
```

## Remarks

For child shapes of a group shape and child shapes of an Office Math object always returns `null`.

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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
