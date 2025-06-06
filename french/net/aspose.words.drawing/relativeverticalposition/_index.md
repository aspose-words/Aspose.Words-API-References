---
title: RelativeVerticalPosition Enum
linktitle: RelativeVerticalPosition
articleTitle: RelativeVerticalPosition
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Drawing.RelativeVerticalPosition pour définir efficacement le positionnement vertical des formes et des cadres de texte et améliorer la mise en page des documents.
type: docs
weight: 1600
url: /fr/net/aspose.words.drawing/relativeverticalposition/
---
## RelativeVerticalPosition enumeration

Spécifie à quoi est relative la position verticale d'une forme ou d'un cadre de texte.

```csharp
public enum RelativeVerticalPosition
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Margin | `0` | Spécifie que le positionnement vertical doit être relatif aux marges de la page. |
| Page | `1` | L'objet est positionné par rapport au bord supérieur de la page. |
| Paragraph | `2` | L'objet est positionné par rapport au haut du paragraphe qui contient l'ancre. |
| Line | `3` | Sans papiers. |
| TopMargin | `4` | Spécifie que le positionnement vertical doit être relatif à la marge supérieure de la page actuelle. |
| BottomMargin | `5` | Spécifie que le positionnement vertical doit être relatif à la marge inférieure de la page actuelle. |
| InsideMargin | `6` | Spécifie que le positionnement vertical doit être relatif à la marge intérieure de la page actuelle. |
| OutsideMargin | `7` | Spécifie que le positionnement vertical doit être relatif à la marge extérieure de la page actuelle. |
| TableDefault | `0` | La valeur par défaut estMargin |
| TextFrameDefault | `2` | La valeur par défaut estParagraph |

## Exemples

Montre comment insérer une image flottante au centre d'une page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérez une image flottante qui apparaîtra derrière le texte superposé et alignez-la au centre de la page.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Montre comment insérer une image et l'utiliser comme filigrane.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérez l'image dans l'en-tête afin qu'elle soit visible sur chaque page.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Placez l'image au centre de la page.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

### Voir également

* property [RelativeVerticalPosition](../shapebase/relativeverticalposition/)
* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
