---
title: ImageSaveOptions.ThresholdForFloydSteinbergDithering
second_title: Referencia de API de Aspose.Words para .NET
description: ImageSaveOptions propiedad. Obtiene o establece el umbral que determina el valor del error de binarización en el método FloydSteinberg. cuandoImageBinarizationMethod es ImageBinarizationMethod.FloydSteinbergDithering.
type: docs
weight: 150
url: /es/net/aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/
---
## ImageSaveOptions.ThresholdForFloydSteinbergDithering property

Obtiene o establece el umbral que determina el valor del error de binarización en el método Floyd-Steinberg. cuando[`ImageBinarizationMethod`](../../imagebinarizationmethod/) es ImageBinarizationMethod.FloydSteinbergDithering.

```csharp
public byte ThresholdForFloydSteinbergDithering { get; set; }
```

### Observaciones

El valor predeterminado es 128.

### Ejemplos

Muestra cómo establecer el umbral de error de binarización TIFF cuando se usa el método Floyd-Steinberg para representar una imagen TIFF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Cuando guardamos el documento como TIFF, podemos pasar un objeto SaveOptions a
// ajustar el tramado que Aspose.Words aplicará al renderizar esta imagen.
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
* espacio de nombres [Aspose.Words.Saving](../../imagesaveoptions/)
* asamblea [Aspose.Words](../../../)


