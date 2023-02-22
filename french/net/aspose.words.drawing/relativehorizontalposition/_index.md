---
title: Enum RelativeHorizontalPosition
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Drawing.RelativeHorizontalPosition énumération. Spécifie à quoi est relative la position horizontale dune forme ou dun bloc de texte.
type: docs
weight: 1060
url: /fr/net/aspose.words.drawing/relativehorizontalposition/
---
## RelativeHorizontalPosition enumeration

Spécifie à quoi est relative la position horizontale d'une forme ou d'un bloc de texte.

```csharp
public enum RelativeHorizontalPosition
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Margin | `0` | Spécifie que le positionnement horizontal doit être relatif aux marges de la page. |
| Page | `1` | L'objet est positionné par rapport au bord gauche de la page. |
| Column | `2` | L'objet est positionné par rapport au côté gauche de la colonne. |
| Character | `3` | L'objet est positionné par rapport au côté gauche du paragraphe. |
| LeftMargin | `4` | Spécifie que le positionnement horizontal doit être relatif à la marge gauche de la page. |
| RightMargin | `5` | Spécifie que le positionnement horizontal doit être relatif à la marge droite de la page. |
| InsideMargin | `6` | Spécifie que le positionnement horizontal doit être relatif à la marge intérieure de la page actuelle (la marge de gauche sur les pages impaires, de droite sur les pages paires). |
| OutsideMargin | `7` | Spécifie que le positionnement horizontal doit être relatif à la marge extérieure de la page actuelle (la marge droite sur les pages impaires, à gauche sur les pages paires). |
| Default | `2` | La valeur par défaut estColumn . |

### Exemples

Montre comment insérer une image flottante au centre d'une page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère une image flottante qui apparaîtra derrière le texte superposé et l'aligne au centre de la page.
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
Image image = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(image);
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Place l'image au centre de la page.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

Montre comment insérer une image et l'utiliser comme filigrane (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérez l'image dans l'en-tête afin qu'elle soit visible sur chaque page.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

using (SKBitmap image = SKBitmap.Decode(ImageDir + "Transparent background logo.png"))
{
    builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
    Shape shape = builder.InsertImage(image);
    shape.WrapType = WrapType.None;
    shape.BehindText = true;

    // Place l'image au centre de la page.
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
    shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
    shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
    shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermarkNetStandard2.docx");
```

### Voir également

* property [RelativeHorizontalPosition](../shapebase/relativehorizontalposition/)
* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)


