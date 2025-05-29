---
title: LayoutFlow Enum
linktitle: LayoutFlow
articleTitle: LayoutFlow
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Drawing.LayoutFlow pour contrôler la mise en page du texte dans les zones de texte, améliorant ainsi la conception et la lisibilité de votre document sans effort.
type: docs
weight: 1430
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

## Exemples

Montre comment ajouter du texte à une zone de texte et modifier son orientation

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textbox = new Shape(doc, ShapeType.TextBox)
{
    Width = 100,
    Height = 100
};
textbox.TextBox.LayoutFlow = LayoutFlow.BottomToTop;

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
