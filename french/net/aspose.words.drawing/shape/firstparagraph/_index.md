---
title: Shape.FirstParagraph
linktitle: FirstParagraph
articleTitle: FirstParagraph
second_title: Aspose.Words pour .NET
description: Récupérez facilement le premier paragraphe d'une forme. Améliorez la mise en page de votre document grâce à notre fonctionnalité « Premier paragraphe de forme » facile à utiliser.
type: docs
weight: 70
url: /fr/net/aspose.words.drawing/shape/firstparagraph/
---
## Shape.FirstParagraph property

Obtient le premier paragraphe de la forme.

```csharp
public Paragraph FirstParagraph { get; }
```

## Exemples

Montre comment créer et formater une zone de texte.

```csharp
Document doc = new Document();

// Créer une zone de texte flottante.
Shape textBox = new Shape(doc, ShapeType.TextBox);
textBox.WrapType = WrapType.None;
textBox.Height = 50;
textBox.Width = 200;

// Définissez l'alignement horizontal et vertical du texte à l'intérieur de la forme.
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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Shape](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
