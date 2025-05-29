---
title: Shape.FirstParagraph
linktitle: FirstParagraph
articleTitle: FirstParagraph
second_title: Aspose.Words für .NET
description: Rufen Sie mühelos den ersten Absatz einer Form ab. Optimieren Sie das Layout Ihres Dokuments mit unserer benutzerfreundlichen Funktion „Form – Erster Absatz“.
type: docs
weight: 70
url: /de/net/aspose.words.drawing/shape/firstparagraph/
---
## Shape.FirstParagraph property

Ruft den ersten Absatz in der Form ab.

```csharp
public Paragraph FirstParagraph { get; }
```

## Beispiele

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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Shape](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
