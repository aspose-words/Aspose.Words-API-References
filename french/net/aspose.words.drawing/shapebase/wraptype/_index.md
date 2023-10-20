---
title: ShapeBase.WrapType
linktitle: WrapType
articleTitle: WrapType
second_title: Aspose.Words pour .NET
description: ShapeBase WrapType propriété. Définit si la forme est en ligne ou flottante. Pour les formes flottantes définit le mode dhabillage du texte autour de la forme en C#.
type: docs
weight: 600
url: /fr/net/aspose.words.drawing/shapebase/wraptype/
---
## ShapeBase.WrapType property

Définit si la forme est en ligne ou flottante. Pour les formes flottantes, définit le mode d'habillage du texte autour de la forme.

```csharp
public WrapType WrapType { get; set; }
```

## Remarques

La valeur par défaut estNone.

N'a d'effet que sur les formes de niveau supérieur.

## Exemples

Montre comment insérer une image flottante au centre d’une page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère une image flottante qui apparaîtra derrière le texte superposé et alignez-la au centre de la page.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
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

* enum [WrapType](../../wraptype/)
* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
