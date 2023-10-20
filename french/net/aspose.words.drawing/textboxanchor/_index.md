---
title: TextBoxAnchor Enum
linktitle: TextBoxAnchor
articleTitle: TextBoxAnchor
second_title: Aspose.Words pour .NET
description: Aspose.Words.Drawing.TextBoxAnchor énumération. Spécifie les valeurs utilisées pour lalignement vertical du texte de forme en C#.
type: docs
weight: 1330
url: /fr/net/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enumeration

Spécifie les valeurs utilisées pour l'alignement vertical du texte de forme.

```csharp
public enum TextBoxAnchor
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Top | `0` | Le texte est aligné en haut de la zone de texte. |
| Middle | `1` | Le texte est aligné au milieu de la zone de texte. |
| Bottom | `2` | Le texte est aligné en bas de la zone de texte. |
| TopCentered | `3` | Le texte est aligné en haut au centre de la zone de texte. |
| MiddleCentered | `4` | Le texte est aligné au milieu de la zone de texte. |
| BottomCentered | `5` | Le texte est aligné en bas au centre de la zone de texte. |
| TopBaseline | `6` | Le texte est aligné sur la ligne de base supérieure de la zone de texte. |
| BottomBaseline | `7` | Le texte est aligné sur la ligne de base inférieure de la zone de texte. |
| TopCenteredBaseline | `8` | Le texte est aligné sur la ligne de base centrée en haut de la zone de texte. |
| BottomCenteredBaseline | `9` | Le texte est aligné sur la ligne de base centrée en bas de la zone de texte. |

## Exemples

Montre comment aligner verticalement le contenu du texte d’une zone de texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// Définissez la propriété "VerticalAnchor" sur "TextBoxAnchor.Top" pour
// aligne le texte de cette zone de texte avec le côté supérieur de la forme.
// Définissez la propriété "VerticalAnchor" sur "TextBoxAnchor.Middle" pour
// aligne le texte de cette zone de texte au centre de la forme.
// Définissez la propriété "VerticalAnchor" sur "TextBoxAnchor.Bottom" pour
// aligne le texte de cette zone de texte au bas de la forme.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// L'alignement vertical du texte à l'intérieur des zones de texte est disponible à partir de Microsoft Word 2007.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
