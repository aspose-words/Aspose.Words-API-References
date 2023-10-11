---
title: Enum ImageBinarizationMethod
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.ImageBinarizationMethod énumération. Spécifie la méthode utilisée pour binariser limage.
type: docs
weight: 5200
url: /fr/net/aspose.words.saving/imagebinarizationmethod/
---
## ImageBinarizationMethod enumeration

Spécifie la méthode utilisée pour binariser l'image.

```csharp
public enum ImageBinarizationMethod
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Threshold | `0` | Spécifie la méthode de seuil. |
| FloydSteinbergDithering | `1` | Spécifie le tramage à l'aide de la méthode de diffusion d'erreur Floyd-Steinberg. |

### Exemples

Montre comment définir le seuil d’erreur de binarisation TIFF lors de l’utilisation de la méthode Floyd-Steinberg pour restituer une image TIFF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Lorsque nous enregistrons le document au format TIFF, nous pouvons passer un objet SaveOptions à
// ajuste le tramage qu'Aspose.Words appliquera lors du rendu de cette image.
// La valeur par défaut de la propriété "ThresholdForFloydSteinbergDithering" est 128.
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

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)


