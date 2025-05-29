---
title: ImageSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words pour .NET
description: Découvrez la propriété SaveFormat d'ImageSaveOptions pour enregistrer facilement vos documents aux formats TIFF, PNG, JPEG, etc. Optimisez votre flux de travail dès aujourd'hui !
type: docs
weight: 140
url: /fr/net/aspose.words.saving/imagesaveoptions/saveformat/
---
## ImageSaveOptions.SaveFormat property

Spécifie le format dans lequel les pages ou les formes du document rendu seront enregistrées si cet objet d'options d'enregistrement est utilisé. Peut être un raster Tiff ,Png ,Bmp , Jpeg ou vecteurEmf ,Eps , WebP ,Svg .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Remarques

Le nombre d’autres options dépend du format sélectionné.

Il est également possible d'enregistrer au format SVG via[`ImageSaveOptions`](../) et via[`SvgSaveOptions`](../../svgsaveoptions/).

## Exemples

Montre comment modifier l'image pendant qu'Aspose.Words convertit un document en un seul.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Lorsque nous enregistrons le document sous forme d'image, nous pouvons passer un objet SaveOptions à
// modifier l'image pendant que l'opération de sauvegarde la rend.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    // Nous pouvons ajuster ces propriétés pour modifier la luminosité et le contraste de l'image.
    // Les deux sont sur une échelle de 0 à 1 et sont à 0,5 par défaut.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // Nous pouvons ajuster la résolution horizontale et verticale avec ces propriétés.
    // Cela affectera les dimensions de l'image.
    // La valeur par défaut de ces propriétés est 96,0, pour une résolution de 96 dpi.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // Nous pouvons redimensionner l'image grâce à cette propriété. La valeur par défaut est 1,0, pour une mise à l'échelle de 100 %.
    // Nous pouvons utiliser cette propriété pour annuler tout changement dans les dimensions de l'image que provoquerait un changement de résolution.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
