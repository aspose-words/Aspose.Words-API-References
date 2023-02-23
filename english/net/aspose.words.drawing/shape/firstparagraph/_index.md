---
title: Shape.FirstParagraph
linktitle: FirstParagraph
second_title: Aspose.Words for .NET API Reference
description: Shape property. Gets the first paragraph in the shape in C#.
type: docs
weight: 60
url: /net/aspose.words.drawing/shape/firstparagraph/
---
## Shape.FirstParagraph property

Gets the first paragraph in the shape.

```csharp
public Paragraph FirstParagraph { get; }
```

## Examples

Shows how to create and format a text box.

```csharp
Document doc = new Document();

// Create a floating text box.
Shape textBox = new Shape(doc, ShapeType.TextBox);
textBox.WrapType = WrapType.None;
textBox.Height = 50;
textBox.Width = 200;

// Set the horizontal, and vertical alignment of the text inside the shape.
textBox.HorizontalAlignment = HorizontalAlignment.Center;
textBox.VerticalAlignment = VerticalAlignment.Top;

// Add a paragraph to the text box and add a run of text that the text box will display.
textBox.AppendChild(new Paragraph(doc));
Paragraph para = textBox.FirstParagraph;
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;
Run run = new Run(doc);
run.Text = "Hello world!";
para.AppendChild(run);

doc.FirstSection.Body.FirstParagraph.AppendChild(textBox);

doc.Save(ArtifactsDir + "Shape.CreateTextBox.docx");
```

### See Also

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Shape](../)
* namespace [Aspose.Words.Drawing](../../shape/)
* assembly [Aspose.Words](../../../)
