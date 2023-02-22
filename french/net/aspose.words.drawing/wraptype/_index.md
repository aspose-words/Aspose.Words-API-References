---
title: Enum WrapType
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Drawing.WrapType énumération. Spécifie la manière dont le texte senroule autour dune forme ou dune image.
type: docs
weight: 1250
url: /fr/net/aspose.words.drawing/wraptype/
---
## WrapType enumeration

Spécifie la manière dont le texte s'enroule autour d'une forme ou d'une image.

```csharp
public enum WrapType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `3` | Aucun habillage de texte autour de la forme. La forme est placée derrière ou devant le texte. |
| Inline | `0` | La forme reste sur le même calque que le texte et est traitée comme un caractère. |
| TopBottom | `1` | Le texte s'arrête en haut de la forme et redémarre sur la ligne sous la forme. |
| Square | `2` | Enveloppe le texte autour de tous les côtés de la zone de délimitation carrée de la forme. |
| Tight | `4` | S'enroule étroitement autour des bords de la forme, au lieu de s'enrouler autour de la boîte englobante. |
| Through | `5` | Identique à Tight, mais s'enroule à l'intérieur de toutes les parties de la forme qui sont ouvertes. |

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

* property [WrapType](../shapebase/wraptype/)
* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)


