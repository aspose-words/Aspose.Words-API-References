---
title: Story.FirstParagraph
linktitle: FirstParagraph
articleTitle: FirstParagraph
second_title: Aspose.Words för .NET
description: Story FirstParagraph fast egendom. Får första stycket i berättelsen i C#.
type: docs
weight: 10
url: /sv/net/aspose.words/story/firstparagraph/
---
## Story.FirstParagraph property

Får första stycket i berättelsen.

```csharp
public Paragraph FirstParagraph { get; }
```

## Exempel

Visar hur man formaterar en serie text med dess teckensnittsegenskap.

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

Visar hur man skapar och formaterar en textruta.

```csharp
Document doc = new Document();

// Skapa en flytande textruta.
Shape textBox = new Shape(doc, ShapeType.TextBox);
textBox.WrapType = WrapType.None;
textBox.Height = 50;
textBox.Width = 200;

// Ställ in den horisontella och vertikala justeringen av texten inuti formen.
textBox.HorizontalAlignment = HorizontalAlignment.Center;
textBox.VerticalAlignment = VerticalAlignment.Top;

// Lägg till ett stycke i textrutan och lägg till en serie text som textrutan kommer att visa.
textBox.AppendChild(new Paragraph(doc));
Paragraph para = textBox.FirstParagraph;
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;
Run run = new Run(doc);
run.Text = "Hello world!";
para.AppendChild(run);

doc.FirstSection.Body.FirstParagraph.AppendChild(textBox);

doc.Save(ArtifactsDir + "Shape.CreateTextBox.docx");
```

### Se även

* class [Paragraph](../../paragraph/)
* class [Story](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
