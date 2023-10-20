---
title: ImageSaveOptions.ThresholdForFloydSteinbergDithering
linktitle: ThresholdForFloydSteinbergDithering
articleTitle: ThresholdForFloydSteinbergDithering
second_title: Aspose.Words para .NET
description: ImageSaveOptions ThresholdForFloydSteinbergDithering propiedad. Obtiene o establece el umbral que determina el valor del error de binarización en el método FloydSteinberg. cuandoImageBinarizationMethod esFloydSteinbergDithering  en C#.
type: docs
weight: 160
url: /es/net/aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/
---
## ImageSaveOptions.ThresholdForFloydSteinbergDithering property

Obtiene o establece el umbral que determina el valor del error de binarización en el método Floyd-Steinberg. cuando[`ImageBinarizationMethod`](../../imagebinarizationmethod/) esFloydSteinbergDithering .

```csharp
public byte ThresholdForFloydSteinbergDithering { get; set; }
```

## Observaciones

El valor predeterminado es 128.

## Ejemplos

Muestra cómo configurar el umbral de error de binarización TIFF cuando se utiliza el método Floyd-Steinberg para representar una imagen TIFF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Cuando guardamos el documento como TIFF, podemos pasar un objeto SaveOptions a
// ajusta el tramado que aplicará Aspose.Words al renderizar esta imagen.
// El valor predeterminado de la propiedad "ThresholdForFloydSteinbergDithering" es 128.
// Los valores más altos tienden a producir imágenes más oscuras.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff)
{
    TiffCompression = TiffCompression.Ccitt3,
    TiffBinarizationMethod = ImageBinarizationMethod.FloydSteinbergDithering,
    ThresholdForFloydSteinbergDithering = 240
};

doc.Save(ArtifactsDir + "ImageSaveOptions.FloydSteinbergDithering.tiff", options);
```

### Ver también

* class [ImageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
