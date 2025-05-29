---
title: TextBox.InternalMarginRight
linktitle: InternalMarginRight
articleTitle: InternalMarginRight
second_title: Aspose.Words pour .NET
description: Découvrez la propriété TextBox InternalMarginRight pour personnaliser vos formes avec des marges droites précises en points pour une flexibilité de conception améliorée.
type: docs
weight: 40
url: /fr/net/aspose.words.drawing/textbox/internalmarginright/
---
## TextBox.InternalMarginRight property

Spécifie la marge intérieure droite en points pour une forme.

```csharp
public double InternalMarginRight { get; set; }
```

## Remarques

La valeur par défaut est 1/10 pouce.

## Exemples

Montre comment définir des marges internes pour une zone de texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer une autre zone de texte avec des marges spécifiques.
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
