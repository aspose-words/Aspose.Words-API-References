---
title: ImageSaveOptions.HorizontalResolution
linktitle: HorizontalResolution
articleTitle: HorizontalResolution
second_title: Aspose.Words para .NET
description: Descubra la propiedad ImageSaveOptions HorizontalResolution para ajustar fácilmente la calidad de la imagen en DPI para obtener una claridad y detalle óptimos en sus proyectos.
type: docs
weight: 30
url: /es/net/aspose.words.saving/imagesaveoptions/horizontalresolution/
---
## ImageSaveOptions.HorizontalResolution property

Obtiene o establece la resolución horizontal de las imágenes generadas, en puntos por pulgada.

```csharp
public float HorizontalResolution { get; set; }
```

## Observaciones

Esta propiedad solo tiene efecto al guardar en formatos de imagen rasterizada y afecta el tamaño de salida en píxeles.

El valor predeterminado es 96.

## Ejemplos

Muestra cómo editar la imagen mientras Aspose.Words convierte un documento en uno.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Cuando guardamos el documento como una imagen, podemos pasar un objeto SaveOptions a
// edita la imagen mientras se procesa la operación de guardado.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    //Podemos ajustar estas propiedades para cambiar el brillo y el contraste de la imagen.
    //Ambos están en una escala de 0 a 1 y están en 0,5 por defecto.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    //Podemos ajustar la resolución horizontal y vertical con estas propiedades.
    // Esto afectará las dimensiones de la imagen.
    //El valor predeterminado para estas propiedades es 96.0, para una resolución de 96 ppp.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    Podemos escalar la imagen usando esta propiedad. El valor predeterminado es 1.0, para un escalado del 100%.
    //Podemos usar esta propiedad para negar cualquier cambio en las dimensiones de la imagen que pudiera causar el cambio de la resolución.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### Ver también

* class [ImageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
