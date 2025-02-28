---
title: Shape.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words for .NET
description: Access the LastParagraph property to easily retrieve the final paragraph in your shape, enhancing your document's layout and readability.
type: docs
weight: 130
url: /net/aspose.words.drawing/shape/lastparagraph/
---
## Shape.LastParagraph property

Gets the last paragraph in the shape.

```csharp
public Paragraph LastParagraph { get; }
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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Shape](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
