---
title: ImageSaveOptions.PixelFormat
linktitle: PixelFormat
articleTitle: PixelFormat
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ImageSaveOptions PixelFormat pour personnaliser facilement le format de pixel de vos images générées pour une qualité et des performances optimales.
type: docs
weight: 120
url: /fr/net/aspose.words.saving/imagesaveoptions/pixelformat/
---
## ImageSaveOptions.PixelFormat property

Obtient ou définit le format de pixel pour les images générées.

```csharp
public ImagePixelFormat PixelFormat { get; set; }
```

## Remarques

Cette propriété n'a d'effet que lors de l'enregistrement dans des formats d'image raster.

La valeur par défaut estFormat32BppArgb.

Le format de pixel de l'image de sortie peut différer de la valeur définie en raison du travail de GDI+.

## Exemples

Montre comment sélectionner un débit de bits par pixel avec lequel restituer un document en image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Lorsque nous enregistrons le document sous forme d'image, nous pouvons passer un objet SaveOptions à
// sélectionnez un format de pixel pour l'image que l'opération de sauvegarde générera.
// Différents débits de bits par pixel affecteront la qualité et la taille du fichier de l'image générée.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PixelFormat = imagePixelFormat;

// Nous pouvons cloner des instances ImageSaveOptions.
Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

### Voir également

* enum [ImagePixelFormat](../../imagepixelformat/)
* class [ImageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
