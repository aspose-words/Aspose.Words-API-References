---
title: TextBox.LayoutFlow
second_title: Référence de l'API Aspose.Words pour .NET
description: TextBox propriété. Détermine le flux de la disposition du texte dans une forme.
type: docs
weight: 60
url: /fr/net/aspose.words.drawing/textbox/layoutflow/
---
## TextBox.LayoutFlow property

Détermine le flux de la disposition du texte dans une forme.

```csharp
public LayoutFlow LayoutFlow { get; set; }
```

### Remarques

La valeur par défaut estHorizontal.

### Exemples

Montre comment définir l'orientation du texte dans une zone de texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Déplacez le générateur de document à l'intérieur du TextBox et ajoutez du texte.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Définissez la propriété "LayoutFlow" pour définir une orientation pour le contenu textuel de cette zone de texte.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

### Voir également

* enum [LayoutFlow](../../layoutflow/)
* class [TextBox](../)
* espace de noms [Aspose.Words.Drawing](../../textbox/)
* Assemblée [Aspose.Words](../../../)


