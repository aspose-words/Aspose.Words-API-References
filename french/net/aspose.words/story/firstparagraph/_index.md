---
title: Story.FirstParagraph
linktitle: FirstParagraph
articleTitle: FirstParagraph
second_title: Aspose.Words pour .NET
description: Story FirstParagraph propriété. Obtient le premier paragraphe de lhistoire en C#.
type: docs
weight: 10
url: /fr/net/aspose.words/story/firstparagraph/
---
## Story.FirstParagraph property

Obtient le premier paragraphe de l'histoire.

```csharp
public Paragraph FirstParagraph { get; }
```

## Exemples

Montre comment formater une séquence de texte à l’aide de sa propriété font.

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

Montre comment créer et formater une zone de texte.

```csharp
Document doc = new Document();

// Crée une zone de texte flottante.
Shape textBox = new Shape(doc, ShapeType.TextBox);
textBox.WrapType = WrapType.None;
textBox.Height = 50;
textBox.Width = 200;

// Définit l'alignement horizontal et vertical du texte à l'intérieur de la forme.
textBox.HorizontalAlignment = HorizontalAlignment.Center;
textBox.VerticalAlignment = VerticalAlignment.Top;

// Ajoutez un paragraphe à la zone de texte et ajoutez une séquence de texte que la zone de texte affichera.
textBox.AppendChild(new Paragraph(doc));
Paragraph para = textBox.FirstParagraph;
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;
Run run = new Run(doc);
run.Text = "Hello world!";
para.AppendChild(run);

doc.FirstSection.Body.FirstParagraph.AppendChild(textBox);

doc.Save(ArtifactsDir + "Shape.CreateTextBox.docx");
```

### Voir également

* class [Paragraph](../../paragraph/)
* class [Story](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
