---
title: Enum TextBoxWrapMode
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Drawing.TextBoxWrapMode énumération. Spécifie comment le texte shabille à lintérieur dune forme.
type: docs
weight: 1190
url: /fr/net/aspose.words.drawing/textboxwrapmode/
---
## TextBoxWrapMode enumeration

Spécifie comment le texte s'habille à l'intérieur d'une forme.

```csharp
public enum TextBoxWrapMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Square | `0` | Le texte rentre dans une forme. |
| None | `2` | Le texte ne rentre pas dans une forme. |

### Exemples

Montre comment définir un mode d'habillage pour le contenu d'une zone de texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 300, 300);
TextBox textBox = textBoxShape.TextBox;

// Définissez la propriété "TextBoxWrapMode" sur "TextBoxWrapMode.None" pour augmenter la largeur de la zone de texte
// pour contenir du texte, s'il est assez grand.
// Définissez la propriété "TextBoxWrapMode" sur "TextBoxWrapMode.Square" pour
// enveloppe tout le texte à l'intérieur de la zone de texte, en préservant ses dimensions.
textBox.TextBoxWrapMode = textBoxWrapMode;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Font.Size = 32;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "Shape.TextBoxContentsWrapMode.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)


