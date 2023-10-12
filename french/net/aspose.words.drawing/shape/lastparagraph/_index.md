---
title: Shape.LastParagraph
second_title: Référence de l'API Aspose.Words pour .NET
description: Shape propriété. Obtient le dernier paragraphe de la forme.
type: docs
weight: 120
url: /fr/net/aspose.words.drawing/shape/lastparagraph/
---
## Shape.LastParagraph property

Obtient le dernier paragraphe de la forme.

```csharp
public Paragraph LastParagraph { get; }
```

### Exemples

Montre comment définir l’orientation du texte à l’intérieur d’une zone de texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Déplacez le générateur de documents à l'intérieur de la TextBox et ajoutez du texte.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Définissez la propriété "LayoutFlow" pour définir une orientation pour le contenu du texte de cette zone de texte.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

### Voir également

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Shape](../)
* espace de noms [Aspose.Words.Drawing](../../shape/)
* Assemblée [Aspose.Words](../../../)


