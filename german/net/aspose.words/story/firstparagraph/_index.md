---
title: Story.FirstParagraph
linktitle: FirstParagraph
articleTitle: FirstParagraph
second_title: Aspose.Words für .NET
description: Entdecken Sie die Story FirstParagraph-Eigenschaft, um ganz einfach den ersten Absatz einer Story zu extrahieren und so Ihren Inhalt und die Benutzerinteraktion zu verbessern.
type: docs
weight: 10
url: /de/net/aspose.words/story/firstparagraph/
---
## Story.FirstParagraph property

Ruft den ersten Absatz der Geschichte ab.

```csharp
public Paragraph FirstParagraph { get; }
```

## Beispiele

Zeigt, wie ein Textlauf mithilfe seiner Schriftarteigenschaft formatiert wird.

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

Zeigt, wie ein Textfeld erstellt und formatiert wird.

```csharp
Document doc = new Document();

// Erstellen Sie ein schwebendes Textfeld.
Shape textBox = new Shape(doc, ShapeType.TextBox);
textBox.WrapType = WrapType.None;
textBox.Height = 50;
textBox.Width = 200;

// Legen Sie die horizontale und vertikale Ausrichtung des Textes innerhalb der Form fest.
textBox.HorizontalAlignment = HorizontalAlignment.Center;
textBox.VerticalAlignment = VerticalAlignment.Top;

// Fügen Sie dem Textfeld einen Absatz und einen Textlauf hinzu, der im Textfeld angezeigt wird.
textBox.AppendChild(new Paragraph(doc));
Paragraph para = textBox.FirstParagraph;
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;
Run run = new Run(doc);
run.Text = "Hello world!";
para.AppendChild(run);

doc.FirstSection.Body.FirstParagraph.AppendChild(textBox);

doc.Save(ArtifactsDir + "Shape.CreateTextBox.docx");
```

### Siehe auch

* class [Paragraph](../../paragraph/)
* class [Story](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
