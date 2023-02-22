---
title: PageSetup.PageHeight
second_title: Référence de l'API Aspose.Words pour .NET
description: PageSetup propriété. Renvoie ou définit la hauteur de la page en points.
type: docs
weight: 300
url: /fr/net/aspose.words/pagesetup/pageheight/
---
## PageSetup.PageHeight property

Renvoie ou définit la hauteur de la page en points.

```csharp
public double PageHeight { get; set; }
```

### Exemples

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

* class [PageSetup](../)
* espace de noms [Aspose.Words](../../pagesetup/)
* Assemblée [Aspose.Words](../../../)


