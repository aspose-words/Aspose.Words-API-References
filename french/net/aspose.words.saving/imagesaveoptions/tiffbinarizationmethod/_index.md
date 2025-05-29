---
title: ImageSaveOptions.TiffBinarizationMethod
linktitle: TiffBinarizationMethod
articleTitle: TiffBinarizationMethod
second_title: Aspose.Words pour .NET
description: Découvrez la propriété TiffBinarizationMethod pour ImageSaveOptions. Convertissez facilement des images au format 1 bpp avec la compression CCITT3 ou CCITT4.
type: docs
weight: 170
url: /fr/net/aspose.words.saving/imagesaveoptions/tiffbinarizationmethod/
---
## ImageSaveOptions.TiffBinarizationMethod property

Obtient ou définit la méthode utilisée lors de la conversion des images au format 1 bpp lorsque[`SaveFormat`](../saveformat/) estTiff et [`TiffCompression`](../tiffcompression/) est égal àCcitt3 ouCcitt4 .

```csharp
public ImageBinarizationMethod TiffBinarizationMethod { get; set; }
```

## Remarques

La valeur par défaut estThreshold.

## Exemples

Montre comment définir le seuil d'erreur de binarisation TIFF lors de l'utilisation de la méthode Floyd-Steinberg pour restituer une image TIFF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Lorsque nous enregistrons le document au format TIFF, nous pouvons passer un objet SaveOptions à
// ajustez le tramage qu'Aspose.Words appliquera lors du rendu de cette image.
// La valeur par défaut de la propriété « ThresholdForFloydSteinbergDithering » est 128.
// Des valeurs plus élevées ont tendance à produire des images plus sombres.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff)
{
    TiffCompression = TiffCompression.Ccitt3,
    TiffBinarizationMethod = ImageBinarizationMethod.FloydSteinbergDithering,
    ThresholdForFloydSteinbergDithering = 240
};

doc.Save(ArtifactsDir + "ImageSaveOptions.FloydSteinbergDithering.tiff", options);
```

### Voir également

* enum [ImageBinarizationMethod](../../imagebinarizationmethod/)
* class [ImageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
