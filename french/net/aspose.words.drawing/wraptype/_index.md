---
title: WrapType Enum
linktitle: WrapType
articleTitle: WrapType
second_title: Aspose.Words pour .NET
description: Découvrez comment l'énumération Aspose.Words.Drawing.WrapType améliore l'habillage du texte autour des formes et des images pour la mise en forme professionnelle des documents.
type: docs
weight: 1810
url: /fr/net/aspose.words.drawing/wraptype/
---
## WrapType enumeration

Spécifie comment le texte est enroulé autour d'une forme ou d'une image.

```csharp
public enum WrapType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `3` | Aucun texte n'est inséré autour de la forme. La forme est placée devant ou derrière le texte. |
| Inline | `0` | La forme reste sur le même calque que le texte et est traitée comme un caractère. |
| TopBottom | `1` | Le texte s'arrête en haut de la forme et recommence sur la ligne en dessous de la forme. |
| Square | `2` | Enveloppe le texte autour de tous les côtés du cadre de délimitation carré de la forme. |
| Tight | `4` | S'enroule étroitement autour des bords de la forme, au lieu de s'enrouler autour du cadre de délimitation. |
| Through | `5` | Identique à Tight, mais s'enroule à l'intérieur de toutes les parties de la forme qui sont ouvertes. |

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

* property [WrapType](../shapebase/wraptype/)
* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
