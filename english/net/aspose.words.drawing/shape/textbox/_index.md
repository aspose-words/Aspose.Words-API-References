---
title: Shape.TextBox
linktitle: TextBox
second_title: Aspose.Words for .NET API Reference
description: Shape TextBox property. Defines attributes that specify how text is displayed in a shape in C#.
type: docs
weight: 220
url: /net/aspose.words.drawing/shape/textbox/
---
## TextBox property

Defines attributes that specify how text is displayed in a shape.

```csharp
public TextBox TextBox { get; }
```

## Examples

Shows how to set the orientation of text inside a text box.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Move the document builder to inside the TextBox and add text.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Set the "LayoutFlow" property to set an orientation for the text contents of this text box.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

### See Also

* class [TextBox](../../textbox/)
* class [Shape](../)
* namespace [Aspose.Words.Drawing](../../shape/)
* assembly [Aspose.Words](../../../)
