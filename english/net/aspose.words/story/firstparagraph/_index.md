---
title: Story.FirstParagraph
linktitle: FirstParagraph
articleTitle: FirstParagraph
second_title: Aspose.Words for .NET
description: Discover the Story FirstParagraph property to easily extract the first paragraph of any story, enhancing your content and user engagement.
type: docs
weight: 10
url: /net/aspose.words/story/firstparagraph/
---
## Story.FirstParagraph property

Gets the first paragraph in the story.

```csharp
public Paragraph FirstParagraph { get; }
```

## Examples

Shows how to format a run of text using its font property.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

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

* class [Paragraph](../../paragraph/)
* class [Story](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
