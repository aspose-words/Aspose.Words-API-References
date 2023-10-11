---
title: Story.FirstParagraph
second_title: Aspose.Words für .NET-API-Referenz
description: Story eigendom. Ruft den ersten Absatz in der Geschichte ab.
type: docs
weight: 10
url: /de/net/aspose.words/story/firstparagraph/
---
## Story.FirstParagraph property

Ruft den ersten Absatz in der Geschichte ab.

```csharp
public Paragraph FirstParagraph { get; }
```

### Beispiele

Zeigt, wie eine Textzeile mithilfe ihrer Schriftarteigenschaft formatiert wird.

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

// Erstelle ein schwebendes Textfeld.
Shape textBox = new Shape(doc, ShapeType.TextBox);
textBox.WrapType = WrapType.None;
textBox.Height = 50;
textBox.Width = 200;

// Legen Sie die horizontale und vertikale Ausrichtung des Texts innerhalb der Form fest.
textBox.HorizontalAlignment = HorizontalAlignment.Center;
textBox.VerticalAlignment = VerticalAlignment.Top;

// Fügen Sie dem Textfeld einen Absatz hinzu und fügen Sie eine Textzeile hinzu, die im Textfeld angezeigt wird.
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
* namensraum [Aspose.Words](../../story/)
* Montage [Aspose.Words](../../../)


