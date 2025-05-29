---
title: TextBox.LayoutFlow
linktitle: LayoutFlow
articleTitle: LayoutFlow
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété TextBox LayoutFlow améliore la mise en page du texte dans les formes, améliorant ainsi la flexibilité de conception et la lisibilité de vos projets.
type: docs
weight: 60
url: /fr/net/aspose.words.drawing/textbox/layoutflow/
---
## TextBox.LayoutFlow property

Détermine le flux de la disposition du texte dans une forme.

```csharp
public LayoutFlow LayoutFlow { get; set; }
```

## Remarques

La valeur par défaut estHorizontal.

## Exemples

Montre comment définir l'orientation du texte à l'intérieur d'une zone de texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Déplacez le générateur de documents à l'intérieur de la zone de texte et ajoutez du texte.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Définissez la propriété « LayoutFlow » pour définir une orientation pour le contenu du texte de cette zone de texte.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

### Voir également

* enum [LayoutFlow](../../layoutflow/)
* class [TextBox](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
