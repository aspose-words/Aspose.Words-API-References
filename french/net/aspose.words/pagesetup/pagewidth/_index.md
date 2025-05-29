---
title: PageSetup.PageWidth
linktitle: PageWidth
articleTitle: PageWidth
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PageSetup PageWidth pour ajuster facilement la largeur de la page en points, améliorant ainsi la mise en page de votre document pour une présentation optimale.
type: docs
weight: 340
url: /fr/net/aspose.words/pagesetup/pagewidth/
---
## PageSetup.PageWidth property

Renvoie ou définit la largeur de la page en points.

```csharp
public double PageWidth { get; set; }
```

## Exemples

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

Montre comment insérer une image flottante et spécifier sa position et sa taille.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Configurez la propriété « RelativeHorizontalPosition » de la forme pour traiter la valeur de la propriété « Left »
 // comme la distance horizontale de la forme, en points, à partir du côté gauche de la page.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Définissez la distance horizontale de la forme par rapport au côté gauche de la page sur 100.
shape.Left = 100;

// Utilisez la propriété « RelativeVerticalPosition » de manière similaire pour positionner la forme 80 pt sous le haut de la page.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Définissez la hauteur de la forme, ce qui mettra automatiquement à l'échelle la largeur pour préserver les dimensions.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// Les propriétés « Bottom » et « Right » contiennent les bords inférieur et droit de l'image.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### Voir également

* class [PageSetup](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
