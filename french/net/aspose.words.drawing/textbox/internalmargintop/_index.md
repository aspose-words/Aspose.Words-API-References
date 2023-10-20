---
title: TextBox.InternalMarginTop
linktitle: InternalMarginTop
articleTitle: InternalMarginTop
second_title: Aspose.Words pour .NET
description: TextBox InternalMarginTop propriété. Spécifie la marge supérieure intérieure en points pour une forme en C#.
type: docs
weight: 50
url: /fr/net/aspose.words.drawing/textbox/internalmargintop/
---
## TextBox.InternalMarginTop property

Spécifie la marge supérieure intérieure en points pour une forme.

```csharp
public double InternalMarginTop { get; set; }
```

## Remarques

La valeur par défaut est 1/20 de pouce.

## Exemples

Montre comment définir les marges internes d’une zone de texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère une autre zone de texte avec des marges spécifiques.
Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox = textBoxShape.TextBox;
textBox.InternalMarginTop = 15;
textBox.InternalMarginBottom = 15;
textBox.InternalMarginLeft = 15;
textBox.InternalMarginRight = 15;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text placed according to textbox margins.");

doc.Save(ArtifactsDir + "Shape.TextBoxMargins.docx");
```

### Voir également

* class [TextBox](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
