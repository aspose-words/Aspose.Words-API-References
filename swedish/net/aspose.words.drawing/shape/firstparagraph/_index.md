---
title: Shape.FirstParagraph
linktitle: FirstParagraph
articleTitle: FirstParagraph
second_title: Aspose.Words för .NET
description: Hämta det första stycket i en form utan ansträngning. Förbättra ditt dokuments layout med vår lättanvända funktion Forma första stycke.
type: docs
weight: 70
url: /sv/net/aspose.words.drawing/shape/firstparagraph/
---
## Shape.FirstParagraph property

Hämtar det första stycket i formen.

```csharp
public Paragraph FirstParagraph { get; }
```

## Exempel

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

// Lägg till ett stycke i textrutan och lägg till en textsekvens som textrutan ska visa.
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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Shape](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
