---
title: Enum LayoutFlow
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Drawing.LayoutFlow énumération. Détermine le flux de la disposition du texte dans une zone de texte.
type: docs
weight: 1100
url: /fr/net/aspose.words.drawing/layoutflow/
---
## LayoutFlow enumeration

Détermine le flux de la disposition du texte dans une zone de texte.

```csharp
public enum LayoutFlow
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Horizontal | `0` | Le texte est affiché horizontalement. |
| TopToBottomIdeographic | `1` | Le texte idéographique est affiché verticalement. |
| BottomToTop | `2` | Le texte est affiché verticalement. |
| TopToBottom | `3` | Le texte est affiché verticalement. |
| HorizontalIdeographic | `4` | Le texte idéographique est affiché horizontalement. |
| Vertical | `5` | Le texte est affiché verticalement. |

### Exemples

Montre comment ajouter du texte à une zone de texte et modifier son orientation

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textbox = new Shape(doc, ShapeType.TextBox)
{
    Width = 100, 
    Height = 100,
    TextBox = { LayoutFlow = LayoutFlow.BottomToTop }
};

textbox.AppendChild(new Paragraph(doc));
builder.InsertNode(textbox);

builder.MoveTo(textbox.FirstParagraph);
builder.Write("This text is flipped 90 degrees to the left.");

doc.Save(ArtifactsDir + "Drawing.TextBox.docx");
```

### Voir également

* property [LayoutFlow](../textbox/layoutflow/)
* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)


