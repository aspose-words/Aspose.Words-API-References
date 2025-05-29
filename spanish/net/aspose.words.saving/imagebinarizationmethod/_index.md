---
title: ImageBinarizationMethod Enum
linktitle: ImageBinarizationMethod
articleTitle: ImageBinarizationMethod
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.ImageBinarizationMethod para una binarización de imágenes eficaz. Optimice el procesamiento de sus documentos con técnicas avanzadas.
type: docs
weight: 5950
url: /es/net/aspose.words.saving/imagebinarizationmethod/
---
## ImageBinarizationMethod enumeration

Especifica el método utilizado para binarizar la imagen.

```csharp
public enum ImageBinarizationMethod
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Threshold | `0` | Especifica el método de umbral. |
| FloydSteinbergDithering | `1` | Especifica el tramado utilizando el método de difusión de error Floyd-Steinberg. |

## Ejemplos

Muestra cómo establecer el umbral de error de binarización TIFF cuando se utiliza el método Floyd-Steinberg para renderizar una imagen TIFF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Cuando guardamos el documento como TIFF, podemos pasar un objeto SaveOptions a
// ajusta el tramado que Aspose.Words aplicará al renderizar esta imagen.
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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
