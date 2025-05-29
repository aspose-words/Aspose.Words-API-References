---
title: ImageSaveOptions.ThresholdForFloydSteinbergDithering
linktitle: ThresholdForFloydSteinbergDithering
articleTitle: ThresholdForFloydSteinbergDithering
second_title: Aspose.Words pour .NET
description: Optimisez vos images grâce au seuil ImageSaveOptions pour le tramage Floyd-Steinberg. Contrôlez les erreurs de binarisation pour des résultats exceptionnels lors du traitement d'images.
type: docs
weight: 160
url: /fr/net/aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/
---
## ImageSaveOptions.ThresholdForFloydSteinbergDithering property

Obtient ou définit le seuil qui détermine la valeur de l'erreur de binarisation dans la méthode Floyd-Steinberg. lorsque[`ImageBinarizationMethod`](../../imagebinarizationmethod/) estFloydSteinbergDithering .

```csharp
public byte ThresholdForFloydSteinbergDithering { get; set; }
```

## Remarques

La valeur par défaut est 128.

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

* class [ImageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
