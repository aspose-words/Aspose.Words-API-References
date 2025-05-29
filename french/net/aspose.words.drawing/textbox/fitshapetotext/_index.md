---
title: TextBox.FitShapeToText
linktitle: FitShapeToText
articleTitle: FitShapeToText
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété FitShapeToText de Microsoft Word ajuste automatiquement les formes pour qu'elles s'adaptent parfaitement à votre texte, améliorant ainsi la présentation du document.
type: docs
weight: 10
url: /fr/net/aspose.words.drawing/textbox/fitshapetotext/
---
## TextBox.FitShapeToText property

Détermine si Microsoft Word doit agrandir la forme pour l'adapter au texte.

```csharp
public bool FitShapeToText { get; set; }
```

## Remarques

La valeur par défaut est`FAUX`.

## Exemples

Montre comment redimensionner une zone de texte pour qu'elle s'adapte parfaitement à son contenu.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Appliquez ces valeurs à ces deux membres pour que la forme parente s'adapte
// étroitement autour du contenu du texte, en ignorant les dimensions que nous avons définies.
textBox.FitShapeToText = true;
textBox.TextBoxWrapMode = TextBoxWrapMode.None;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text fit tightly inside textbox.");

doc.Save(ArtifactsDir + "Shape.TextBoxFitShapeToText.docx");
```

### Voir également

* class [TextBox](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
