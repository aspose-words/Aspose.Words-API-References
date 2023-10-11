---
title: TextBox.TextBoxWrapMode
second_title: Référence de l'API Aspose.Words pour .NET
description: TextBox propriété. Détermine la manière dont le texte senroule à lintérieur dune forme.
type: docs
weight: 110
url: /fr/net/aspose.words.drawing/textbox/textboxwrapmode/
---
## TextBox.TextBoxWrapMode property

Détermine la manière dont le texte s'enroule à l'intérieur d'une forme.

```csharp
public TextBoxWrapMode TextBoxWrapMode { get; set; }
```

### Remarques

La valeur par défaut estSquare.

### Exemples

Montre comment définir un mode d’habillage pour le contenu d’une zone de texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 300, 300);
TextBox textBox = textBoxShape.TextBox;

// Définissez la propriété "TextBoxWrapMode" sur "TextBoxWrapMode.None" pour augmenter la largeur de la zone de texte
// pour accueillir du texte, s'il est suffisamment grand.
// Définissez la propriété "TextBoxWrapMode" sur "TextBoxWrapMode.Square" pour
// enveloppe tout le texte à l'intérieur de la zone de texte, en préservant ses dimensions.
textBox.TextBoxWrapMode = textBoxWrapMode;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Font.Size = 32;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "Shape.TextBoxContentsWrapMode.docx");
```

### Voir également

* enum [TextBoxWrapMode](../../textboxwrapmode/)
* class [TextBox](../)
* espace de noms [Aspose.Words.Drawing](../../textbox/)
* Assemblée [Aspose.Words](../../../)


